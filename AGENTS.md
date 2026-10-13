# AGENTS.md — обязательная точка входа ИИ в Blender

## Создание, исправление и переработка любых 3D-моделей — 3D Craft

**До начала любой генерации/правки 3D-модели или её детали** прочитать [docs/3D_CRAFT.md](docs/3D_CRAFT.md) и [PROJECT_INSTRUCTIONS.md](PROJECT_INSTRUCTIONS.md); найти и реально активировать установленный [3D Craft](https://chatgpt.com/plugins/plugins_6acdc74c86888191b2101b657a2e8f8d) (`3d-craft`). Если он отсутствует в данной среде — `BLOCKED`, запросить подключение и не обходить конвейер. Упоминание `@3d-craft` само по себе не гарантирует загрузку.

Процесс: изображение напрямую → локальный Stable Fast 3D → GLB варианты → примерка, сборка и QA 42 ракурсов в Blender → Unity при необходимости. ComfyUI и Rodin не входят в эту технологию; другие задачи поиска/интеграции ассетов не меняются. Беречь оригинал, создавать резервные копии, исправлять только плохие части и аксессуары, вести краткие промежуточные отчёты; при доступности делегирования привлекать субагентов на той же модели/мощности, если поддерживается.

Остальные правила: [PROJECT_INSTRUCTIONS.md](PROJECT_INSTRUCTIONS.md), [PIPELINE.md](PIPELINE.md), [WORKFLOW_AND_PATHS.md](WORKFLOW_AND_PATHS.md), [LOCAL_ASSET_PATHS.md](LOCAL_ASSET_PATHS.md), [ASSET_QA.md](ASSET_QA.md).
