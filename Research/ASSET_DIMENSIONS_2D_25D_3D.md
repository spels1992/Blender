# Расширение поиска: 2D, 2.5D и 3D

Дата: 2026-10-09. Дополнение к FREE_ONLY_POLICY.md и существующим очередям; прежние задачи не отменяются.

## Обязательный охват
- **2D:** спрайты, sprite sheets, тайлсеты, изометрические тайлы, персонажи, враги, предметы, здания, окружение, эффекты, UI, иконки, анимации и покадровые наборы.
- **2.5D:** изометрические и псевдо-3D ассеты в духе Project Zomboid, prerendered 3D→2D sprites, billboard/impostor, многослойный параллакс, 2D персонажи в 3D мире, ортографические сцены. Проверять реальные типы ассетов, не приписывать конкретной игре неподтверждённый пайплайн.
- **3D:** меши, риги, анимации, модульные системы, VFX и окружение.
- **Материалы:** PBR и неполные текстурные наборы для 2D/2.5D/3D с раздельной технической маркировкой.

## Для каждого типа объекта
Искать по возможности 2–3 независимых варианта в каждом применимом измерении (2D/2.5D/3D), а не 2–3 суммарно. Все жанры: survival, RPG, стратегия, ферма, хоррор, шутер, платформер, гонки, головоломки, симулятор и др.

## Поля карточки
asset_type (2D|2.5D|3D|MATERIAL), subformat (spritesheet|tileset|isometric|billboard|mesh|etc), genre_tags, exact_asset_url, creator, exact_license_url, license_version, attribution_required, commercial_use_confirmed, cost_0_rub_confirmed, formats, dimensions_or_polycount, animations, view_angles, pixels_per_unit, unity_pipeline (SpriteRenderer/Tilemap/URP 2D/3D), blender_role (optional for native 2D), source_checked_at, verification_state. Unknown = NOT_VERIFIED, not PASS.

Для 2.5D дополнительно: перспектива/изометрия, количество ракурсов, сортировка по Y/depth, прозрачность, pivot и совместимость с освещением. Для PBR сохранять отдельные поля карт BaseColor, Normal GL/DX, Roughness, Metallic, AO, Height, Alpha, tileability, max_resolution, Blender/Unity URP import; различать fur surface PBR и hair cards/groom geometry.

## Лицензии и хранение
Только 0 ₽ и коммерческое использование; CC0 предпочтительнее, CC BY с атрибуцией, CC BY-SA/неясные условия — LEGAL_REVIEW. Не загружать сторонние архивы в GitHub. Не записывать страницу коллекции как подтверждённый конкретный ассет. Не создавать технический PASS без реального теста.

## Следующие задачи
1. Проанализировать текущие каталоги на покрытие 2D/2.5D/3D и дубли URL.
2. Для очередного типа объекта собрать по 2–3 конкретные авторские страницы на каждый применимый формат.
3. Добавить отдельный машиночитаемый индекс 2D/2.5D и ссылки в основной индекс, не ломая текущую схему.
4. Продолжать материалы/PBR параллельно и фиксировать QA отдельно.
