# Blender → Unity URP: PBR texture pipeline (бесплатно)

**Статус:** инструкция по настройке. Ни одна модель/текстура из индекса ещё не получила подтверждённый импорт в живом проекте Unity.

## Карты и цветовые пространства

| Карта у автора | Blender (Principled BSDF) | Unity URP/Lit | Цветовое пространство |
|---|---|---|---|
| BaseColor / Diffuse / Albedo | Base Color | Base Map | **sRGB** |
| Normal OpenGL / `nor_gl` | Image Texture → Normal Map node → Normal | Normal Map (проверить ориентацию Y на тестовой плоскости) | **Non-Color / Normal map** |
| Normal DirectX / `nor_dx` | Может потребоваться инверсия зелёного канала по результату теста | Normal Map; проверить реальную ориентацию Y и импорт | **Non-Color / Normal map** |
| Roughness | Roughness | URP smoothness = **1 - roughness**; для Metallic workflow часто упаковать в альфа-канал metallic map | **Linear** |
| Metallic / Metalness | Metallic | Metallic (часто R в metallic-map; проверить выбранный workflow/версию URP) | **Linear** |
| Ambient Occlusion / AO | В diffuse или mix/shader по необходимости; отдельного AO-входа Principled BSDF нет | Occlusion Map, проверить упаковку в канал и интенсивность | **Linear** |
| Height / Displacement | Bump/Displacement nodes; настоящий displacement требует поддержки геометрии/рендера | Не все URP/Lit шейдеры применяют displacement без custom Shader Graph; не включать автоматически | **Linear** |
| Opacity / Alpha | Alpha + прозрачность материала | Surface Type Transparent/Cutout в зависимости от версии URP | **Linear alpha / sRGB RGB** |
| Anisotropy Strength/Rotation | Principled BSDF Anisotropic/Anisotropic Rotation, если подходит версии Blender | Штатный URP/Lit может не повторять эффект; требуется Shader Graph или упрощение | **Linear** |

Нормали: Blender в привычных рабочих сценариях часто использует OpenGL-style normal map, но **не следует слепо утверждать**, что любая версия Unity требует только DirectX. На плоскости с выпуклым тестовым рельефом сравнить визуально; при неверной впадине/выпуклости инвертировать **G / Y**, а не случайные каналы.

## Порядок для Blender
1. Проверить **действительный бесплатный архив** на оригинальной странице; сохранить оригинальные лицензионные сведения и автора.
2. Создать материал с Principled BSDF: Color=Albedo sRGB, NormalGL через отдельную ноду `Normal Map` и Image Texture как `Non-Color`, Roughness/Metallic как `Non-Color`.
3. UV: применить масштаб объекта, проверить отсутствующие или перекрывающиеся UV, физическую ширину образца и направления швов.
4. Проверить материал на тестовом шаре, кубе, плоскости под косым светом и на реальном объекте; Tileability — реальный **тест**, а не ожидание по названию.
5. Фактуру кожи, ткани и коры подбирать под **крупность плана**; microdetail normal не компенсирует отсутствие silhouette у меха.

## Перенос в Unity URP
1. Выбрать актуальный URP/Lit для проекта; убедиться, что материал не переключился на Built-in/Standard или розовый missing shader.
2. Albedo в Base Map, normal map импортировать как **Normal map**; если источник DX, а профиль ожидает GL (или наоборот), сверить тестом рельеф и при необходимости инвертировать зелёный канал в бесплатном редакторе изображений/скрипте.
3. Если Metallic workflow: Smoothness = 1 − Roughness. При packing сохранить Metallic в соответствующий канал, Smoothness — в предусмотренный текущим URP профиль (часто альфа Metallic). Проверить по фактической версии URP. AO — отдельно или в соответствующий канал шейдера.
4. Для мобильной игры сначала 1K–2K, mipmaps, платформа-зависимое сжатие (например, ASTC при поддержке); не импортировать **162×8K** наборов сразу.
5. Измерить память и FPS на репрезентативной сцене, особенно если много одинаковых материалов. Использовать атласы, shader variants осознанно.
6. При отсутствии Height в текущем Lit — не обещать параллакс без отдельного шейдера и реального теста.

## Специальные категории
- **Мех/шерсть:** Faux Fur, Teddy, Fleece — текстурный ворс. Для волосатого силуэта нужны hair cards, strand geometry или shell rendering; совместимость с Unity и производительность проверять отдельно.
- **Кора/кирпич/плитка:** направление древесных волокон, ориентация швов и UV-scale имеют значение.
- **Мокрые поверхности:** меняются roughness и нормали, нельзя автоматически считать материал с зелёным оттенком «влажным».
- **Лёд/стекло:** прозрачность, refraction, double-sided и depth write обычно требуют особой настройки Shader Graph/URP; пока таких карточек в индексе нет, не симулировать достижение.
- **Декали:** отличаются от обычных тайлинговых материалов; для URP может требоваться Decal Renderer Feature и совместимый renderer. Проверить поддержку в актуальном Unity.

## Заключение
Публикуем только **документацию, лицензии и источники**. Поля `blender_tested`, `unity_urp_tested`, `available_maps_checked_in_archive` в [INDEX.json](INDEX.json) менять на true только при фактическом испытании и наличии логов/доказательств.
