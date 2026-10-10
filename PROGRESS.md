# Журнал выполнения — Blender Assets Library

## 2026-10-08: цикл 001
- **100/100** микрозадач первичного поиска: открыты официальные страницы с описанием бесплатных наборов, занесены **100 уникальных URL** в Markdown-каталог и JSON-индекс.
- Проверены базовые правила лицензирования на официальных сайтах Kenney, KayKit, Quaternius, Poly Haven, Creative Commons, Fab, Sketchfab, Mixamo и др.
- Категории покрывают персонажей, существ, скелетов, динозавров, животных, машины, корабли, роботов, здания, природу, оружие, мебель, еду, анимации, подземелья и Sci-Fi.
- Созданы правила прав использования, проверки качества, структура категорий и процедура Blender → Unity.
- Добавлен справочник порталов для следующей фазы.
- **Не сделано:** загрузка ZIP, проверка содержимого, проверка моделей Blender, импорт в Unity, замеры FPS, юридическое заключение по каждой лицензии.
- **Особый риск:** новая Quaternius QAL 2026-08-28 при старых CC0 метках; не зеркалировать данные.
- **Следующая очередь:** практические пробы по `ROADMAP_100.md` и расширение каталога уникальными типами существ/моделей.
- Статус записей: `SOURCE_VERIFIED`. Статус интеграции: `NOT_TESTED`.

Все результаты этого цикла сохранены в репозитории. Цель следующего цикла — переход от большой библиотеки ссылок к **отобранным проверенным игровым ресурсам**.

## 2026-10-08: цикл 002 — расширение по типам объектов

- **100/100 последовательных задач каталогизации** сохранены в `Catalog/ObjectTypes/001.md` … `100.md`, каждая отдельным коммитом в GitHub. Темы — 10 групп по 10 часто встречающихся предметов.
- По 3 бесплатных тематических источника на тип: всего 300 привязок к ранее найденным наборам, **не** 300 подтверждённых поштучных моделей.
- После дополнительного поштучного исследования: **167 записей** по **150 различным страницам**, охвачено **88/100 категорий** конкретными CC0-моделями или наборами с перечисленным предметом.
- **12/100** категорий остаются без точного CC0-совпадения: Душевая кабина, Стиральная машина, Картина, Зеркало, Крыша, Светофор, Склад, Гора, Ручей или река, Эльф, Орк, Виверна.
- Подготовлена следующая очередь `Catalog/ObjectTypes/CYCLE_003_QUEUE.json` — **ещё 100 типов** из медицины, школы, ферм, спорта, техников, фэнтези и городских объектов; **в очереди, не выполнены**.
- Пользователь установил жёсткий бюджет 0 ₽. Добавлена [FREE_ONLY_POLICY.md](FREE_ONLY_POLICY.md): только бесплатные для коммерческих игр, без обязательных подписок, платных редакций и платных исходников.
- Статус поштучных находок: `SOURCE_PAGE_VERIFIED`; **содержимое ZIP не изучено**, Unity и Blender **не тестировались**, техническая пригодность ещё неизвестна. Не заявлять работоспособность без испытаний.
- Старые CC0-метки Quaternius vs новая QAL требуют дополнительной лицензионной проверки для конкретного скачивания; не зеркалировать архивы.

[Главный индекс](Catalog/ObjectTypes/INDEX.md) · [JSON-индекс](Catalog/ObjectTypes/index.json) · [167 отдельных записей](Catalog/EXACT_FREE_ASSETS.json).

## 2026-10-08: циклы 002 (уточнение) и 003 (поиск 100 типов)

- Проведено ещё **12 отдельных повторных проверок** старых CC0-пробелов: `Research/C002_GAPS/017.md` и другие номера.
- По циклу 002 обновлено до **176 ссылочных записей по 158 страницам**, **94/100 категорий** имеют хотя бы одну конкретную CC0-страницу, пакет или тег. Остальные 6 требуют более точного поиска; есть бесплатные CC-BY/CC-BY-SA модели эльфа и виверны с обязательной атрибуцией/ограничениями.
- Цикл 003: **100/100** новых карточек исследования сохранены отдельными коммитами `Catalog/Cycle003/001.md ... 100.md`.
- Установлено **42 категории с точными бесплатными ссылками**, из них **18 категорий с >=2 ссылками**, **24 с одной**, **58 категорий пока без точной ссылки**.
- **69 точных ссылочных привязок** и **15 частичных/тематических кандидатов**. Одна страница может относиться к нескольким категориям. Полные показатели: `Catalog/Cycle003/INDEX.json`.
- Никаких платных ресурсов; запрещённые платные опции и генератор с заблокированным скачиванием не засчитаны как пригодные модели.
- **Файлы ассетов не загружались, Blender и Unity не тестировались.** Изучение страниц не даёт права отмечать ресурс `UNITY_TESTED`.
- Следующий этап: закрыть 58 пробелов третьего цикла, добрать независимые варианты до 2–3 на категорию, провести 실제 QA Blender/Unity после скачивания.

## 2026-10-08: цикл C004 — 100 отдельных карточек предметов
- **100/100** новых исследовательских карточек сохранены последовательно в `Research/C004/C004-001.md` … `C004-100.md`.
- **94 уникальные страницы первоисточников**, 6 повторов внутри цикла. **97** карточек с заявленной CC0 и **3** с CC BY-SA и отметкой LEGAL_REVIEW.
- **12** записей о предметах, которые лишь связаны с запрошенным классом; они не засчитываются как точные модели и отдельно помечены в JSON.
- **18** карточек с возможной высокой геометрической сложностью (вплоть до миллионов треугольников); обязательно проверять LOD/производительность.
- Создан единый каталог `Catalog/MASTER_SEARCH_INDEX.json`: **445** связей из четырёх циклов на **406** уникальных страниц после устранения **39** повторов.
- Вся работа основана только на **бесплатных** исходных страницах с заявленной коммерческой лицензией; платные подписки, экспорт и модели исключены.
- Проверено только наличие информации на публичных страницах: **0** реальных испытаний Blender/Unity и **0** скачанных ассетов. Каталог ссылок не равен готовым игровым моделям.
- Следующий приоритет — углубление пробелов, больше вариантов на объект, реальная загрузка/проверка части моделей для Unity без нарушения лицензий.

[Обзор C004](Research/C004/README.md) · [Объединённая база](Catalog/MASTER_INDEX.md).

## 2026-10-08: цикл C005 — 100 последовательных задач уточнения бесплатных моделей
- Отработаны и сохранены **100/100 исследовательских карточек** `Research/C005/C005-001.md ... C005-100.md`, последовательно отдельными коммитами GitHub.
- **24** категории содержат 2+ точных ссылок, **33** — одну, **43** — остаются без точного подтверждения (сохранены GAP); число независимых моделей ещё не проверено по скачанным файлам.
- **98** ссылочных привязок к **90 уникальным точным страницам** (без путаницы с поисковыми порталами), из них **29 совершенно новых страниц** для общего каталога по сравнению с C001-C004.
- [Единая поисковая база](Catalog/MASTER_SEARCH_INDEX.json) теперь: **543** привязки / **435** уникальных страниц / **108** повторов между циклами.
- Приоритет только **полностью бесплатных** источников с законным коммерческим использованием. CC BY требует авторство; CC BY-SA/GPL — отдельная проверка. Quaternius исторический CC0 vs QAL: не применять автоматически.
- Важные результаты: три CC0 подводных аппарата, несколько CC0-алтарей и факелов, новые кактусы CC BY/SA, отдельный CC-BY погрузчик, солярная панель, конструктор аксессуаров OverScore Proxy CC0.
- **0** реальных Blender/Unity импортов и **0** технически проверенных архивов в исследовательской цепочке C005. Никаких ложных PASS.
- Подготовлена **новая очередь 100 задач C006** `Research/C006_QUEUE.json`: 43 пробела, 33 поиска вторых независимых моделей и 24 технических проверки; эта очередь **не выполнена**.
- [Итог C005](Research/C005/README.md) и [структурированные статусы](Research/C005/INDEX.json).

## 2026-10-08: отдельная библиотека PBR-текстур — расширение и восстановление карточек

- Найден и сохранён существующий индекс **119** PBR-текстур (`Materials/INDEX.json`), который не был включён в главный README. Поэтому старые находки **не были посчитаны новыми**.
- **43 новые оригинальные страницы CC0** добавлены как `MAT-120..MAT-162` (новые группы: `FUR_PLUSH` 8, `SOIL_MUD` 10, `GRASS_GROUND` 6, `FOREST_FLOOR` 3, `CONCRETE` 6, `RUBBER_PLASTIC` 6, `MOSS` 3, `LEATHER` 1). Новые карточки сохранены отдельно с коммитами. Источники Poly Haven с бесплатной CC0 лицензией.
- **105 ранее отсутствовавших Markdown-карточек MAT-015..MAT-119** восстановлены из старого JSON-индекса, чтобы навигация работала. `MAT-001..MAT-014` уже были в репозитории. Это техническое исправление, не 105 новых материалов.
- [Текущий человекочитаемый каталог](Materials/INDEX.md): **162 ссылки и 18 категорий**. Данные [JSON](Materials/INDEX.json).
- Добавлены [инструкция Blender → Unity URP](Materials/PIPELINE.md), [QA checklist](Materials/QA_CHECKLIST.md), [README](Materials/README.md) и [следующая очередь 100 текстурных задач](Materials/NEXT_100_QUEUE.json).
- **Особая группа шерсти/меха:** меховые PBR-текстуры различаются с полноценным hair/fur groom, карточками волос и шерстяной геометрией. Они не заменяют объёмные волосы.
- CC0 подтверждена по [официальной лицензии Poly Haven](https://polyhaven.com/license) и [справочнику cgbookcase](https://www.cgbookcase.com/textures/). Лицензионные заявления не равны технической проверке реальных файлов.
- **В этой фазе: 0 архивов скачано, 0 проверок тайлинга, 0 реальных Blender-тестов, 0 проверок Unity URP.** Карты PBR по источнику могут присутствовать, но проверить отдельные архивы всё ещё необходимо.
- Следующий приоритет по материалам: проверить доступные карты у конкретных материалов, искать CC0-лёд, прозрачное стекло, декали, волосы/шерсть животных и стилизованные покрытия; перейти к бесплатным реальным тестам, если доступен тестовый Unity-проект.

## 2026-10-09: расширение глобальных правил + подсчёт объёма текущей базы

- Сохранена новая обязательная [GLOBAL_ASSET_SEARCH_POLICY.md](GLOBAL_ASSET_SEARCH_POLICY.md): **полностью бесплатно / коммерческое использование / минимум 2–3 независимых варианта каждого типа / максимум не ограничен** (поиск не прекращается после трёх); **все 3D, 2.5D, 2D и другие полезные формы**, все стили, жанры и любые легальные сайты. В поиск на равных входят текстуры и материалы (кора, трава, облака, листья, снег, грунт, кирпич, мех, PBR и др.).
- Обновлены README.md, FREE_ONLY_POLICY.md, TAXONOMY.md, Catalog/SOURCE_PORTALS.md, Catalog/MASTER_INDEX.md и текущие очереди Research/C006_QUEUE.json / Materials/NEXT_100_QUEUE.json; верхнее правило имеет приоритет над историческими формулировками «искать только 3D» или «найти 2 и закончить».
- Ежечасное расписание «Поиск моделей и текстур» также обновлено: поиск без верхней границы по форматам/стилям/жанрам/сайтам и учёт размеров скачивания.
- Состав **существующих** URL: 435 уникальных страниц моделей/наборов + 162 уникальные страницы PBR-текстур = **597 URL без пересечений**. 100 авторских наборов Kenney/KayKit/Quaternius, 238 страниц OpenGameArt, 97 страниц Poly Haven в модельном каталоге.
- Фактические размеры **584/597** URL пока не известны. В [аудите](Catalog/DOWNLOAD_SIZE_AUDIT.json) **13 выборочных опубликованных** размеров, неизвестные — null. [Предварительная оценка](Catalog/DOWNLOAD_SIZE_ESTIMATE.md) **~20–80 ГБ** для одной обычной версии каждого ассета, иллюстративный сценарий ~**33,609 ГБ** с явно записанными предположениями. Точная сумма без размеров 584 URL НЕ вычислена и не должна выдаваться за измеренную.
- Новое обязательное поле: download_size_bytes (+ формат/разрешение/источник размера) для расчёта общей потребности в диске после сбора данных; не считать несколько одинаковых архивов дважды и не включать платные скачивания.
- Новые страницы моделей/текстур в этом обновлении не открывались как отдельный новый цикл; работа — исправление политики и аудит каталога, без подмены исследований.

## 2026-10-09: C006 printer + cloud-source expansion (source-only)
- **4 new exact printer model pages**, independent item pages: Poly Pizza CreativeTrio CC0; 3DAssets.dev CC0 AI-assisted (provenance caution, publisher lists 34.7 KB); Sketchfab Red Fox and CG Buzz CC BY (exact license version still to confirm). Recorded in [printer cards](Research/C006/PRINTER_NEW_SOURCES_20261009.json). C006-001 minimum provisionally met; open-ended search continues.
- **3 new independent CC0 cloud resource pages** from WickedInsignia, zelun, Luke.RUSTLTD: transparent cloud textures, 2D sprites, six-face skybox; recorded in [cloud research](Materials/CLOUDS_RESEARCH_20261009.md). No PBR/volumetric equivalence claimed.
- Publisher-displayed sizes: 34.7 KB (printer GLB); 28.5 Mb, 201.8 Mb, 8.7 Mb (cloud archives). **No measured byte counts**, all download_size_bytes=null. None of these 7 URLs were present in original model/material indexes or size audit at search time; not yet incorporated into the master JSON due to blocked large-file write.
- **0 downloaded files, 0 Blender tests, 0 Unity tests**. 2 new research records committed; full master indexes, queue and size audit remain pending sync. Existing audit remains 597 URLs, 584 unknown byte sizes; newly discovered pages not included in that baseline.

## 2026-10-09: глобальные требования, 2D / 2.5D, расчёт размера всей базы

- Пользователь утвердил обязательную политику [GLOBAL_ASSET_SEARCH_POLICY.md](GLOBAL_ASSET_SEARCH_POLICY.md): **все 3D, 2.5D, 2D и другие представления, модели/текстуры/облака/травы/листья, все стили/жанры/источники, исключительно бесплатно для коммерции**. На каждый тип 2–3 независимых варианта **МИНИМУМ**, потолка нет — поиск продолжается и после достижения минимума.
- Расширены root README, FREE_ONLY_POLICY.md, TAXONOMY.md и часовая автоматизация; запрещён фиктивный статус завершения поиска при 2–3 источниках.
- Найдены **42 новые URL CC0** вне прежних 597: **15 изометрических 2.5D** и **27 2D** страниц Kenney/OpenGameArt, включая спрайты/тайлы травы, здания, транспорт, окружение, облака и игровые UI-подсказки. Созданы [42 раздельные карточки](Catalog/Multiformat/README.md), общий [индекс](Catalog/Multiformat/INDEX.json); эти ассеты **не были** в предыдущем индексе.
- Объединённый индекс [MASTER_SEARCH_INDEX.json](Catalog/MASTER_SEARCH_INDEX.json) теперь **477 оригинальных страниц визуальных ресурсов**, **585 ссылочных связей**, 108 повторных привязок. Отдельно [Materials/INDEX.json](Materials/INDEX.json) содержит **162** источника PBR. **Всего 639 разных URL** без пересечения между модельным и материальным списками. Не путать URL с числом независимо проверенных моделей внутри наборов.
- Подсчёт объёма: [человекочитаемая оценка](Catalog/DOWNLOAD_SIZE_ESTIMATE.md) и [аудит всех 639 URL](Catalog/DOWNLOAD_SIZE_AUDIT.json). На **44 страницах** есть округлённые авторские размеры, **595 источников** без размеров; известная подгруппа суммируется до **≈3 455,17 МБ**, но полный вес **НЕИЗВЕСТЕН**. Прогноз при допущениях — около **28,65–34,03 ГБ** для средней смешанной подборки, приблизительно **6,05–262,2 ГБ** по специально заданным лёгкому/тяжёлому сценариям, возможен большой выход за пределы при всех версиях и распаковке. Практический запас — 100 ГБ архивы, 200 ГБ+ распакованные рабочие файлы.
- **Все данные о размере пока взяты с опубликованных страниц, не из фактически скачанных файлов. 0 Unity/Blender тестов новых ресурсов и 0 полных измерений.** Цена 0 ₽, чужие большие архивы в GitHub не копировались.

## 2026-10-09: hourly research — robots and skybox textures
- Seven new CC0 publisher item pages committed: 3 robot 3D models and 4 texture/skybox source pages. Records: `Catalog/Expansion/NEW_3D_ROBOTS_20261009_H4.json` and `Materials/NEW_SKYBOX_SURFACES_20261009_H4.json`.
- The 696-page previous logical index plus seven new URL pages gives 703 logical source URLs pending index merge; publisher-rounded sizes shown for all seven, exact download bytes unknown, no Blender or Unity tests.
- Attempts to write 2D/2.5D records, download-size delta and main summary were blocked; those files remain unchanged. No archives uploaded.

## 2026-10-09 — H6 source research
- Added 20 exact CC0 source pages: 6 2D effects/sprite packs, 1 isometric vehicle sprites pack, 7 3D vehicle/spaceship pages, 6 grass/cloud/PBR material pages.
- New cards: `Research/C006/H6_20261009_2D_VFX.md`, `Research/C006/H6_20261009_3D_VEHICLES.md`, `Materials/H6_20261009_GRASS_CLOUDS_ROOF_RUST.md`.
- Size audit: `Catalog/H6_20261009_SIZE_AUDIT.md`. All 20 have publisher-listed rounded attachment sizes; 0 verified exact byte counts. 602 pre-existing unknown sizes unresolved. Provisional unique page count 738 (718 previous + 20 H6), main indexes merged: master 491, materials 168, audit base 659; logical overlays 738.
- No archives downloaded, no Blender/Unity import tests; 0 new PASS. Source-page counts do not equal independent meshes. Continue open-ended research and merge index overlays.


## 2026-10-09 — H16 recovery, full backup metadata persisted
- Complete pending research metadata recovered and verified by GitHub readback. This is a research **queue**, not canonical adoption or editor PASS.
- 23 records: `Catalog/Expansion/H16_PENDING_FULL_METADATA_20261009.json`; prior URL list: `Catalog/Expansion/H16_PENDING_RECOVERY_20261009.md`.
- Need master index deduplication, individual license/dependency review and canonical card promotion. Exact sizes UNKNOWN/null; Unity/Blender editor NOT_TESTED; no large archives downloaded, no new costs.


## 2026-10-09 — H16 canonical source index reconciliation
- 23/23 H16 recovered source URLs merged into `Catalog/MASTER_SEARCH_INDEX.json` in six small commits; readback confirmed 624 unique indexed URLs (was 601). Full metadata remains in `Catalog/Expansion/H16_PENDING_FULL_METADATA_20261009.json`.
- Source index reconciliation PASS; semantic deduplication, independent license/dependency validation and editor tests still pending. Download sizes UNKNOWN/null; editors NOT_TESTED. No external archives downloaded; no additional spending.

## 2026-10-10: H17/H18 recovery

- Recovered 19 H17 source-page records and 5 H18 source-page records through GitHub Plugin; canonical index merge added 24 previously absent exact URLs.
- H17: `Catalog/Expansion/H17_RECOVERED_19_CC0_PAGES_20261010.json`; H18: `Catalog/Expansion/H18_RECOVERY_5_CC0_PAGES_20261010.json`.
- Vegetation Low Poly was already indexed in `Catalog/Expansion/INDEX_20261009.json`, so it was not duplicated.
- Source pages only; licenses must be reconfirmed before production. Download/Blender/Unity tests NOT_RUN.
