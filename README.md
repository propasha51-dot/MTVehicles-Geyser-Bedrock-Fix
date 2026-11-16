# MTVehicles — Geyser Bedrock Compatibility Fix

**Русский | English below**

## Описание

Исправление совместимости ресурспака MTVehicles с Minecraft Bedrock Edition через Geyser.

Проект основан на Bedrock-порте от **Tydium**:

**Оригинальный проект:** https://github.com/Tydium/MTVehicles-Bedrock-Pack

Большое спасибо Tydium за оригинальную работу по переносу моделей и текстур MTVehicles на Bedrock!

### Проблема

При подключении к Java-серверу через Bedrock:
- Разные машины могли отображаться одной и той же моделью.
- Транспорт мог иметь неправильные текстуры или внешний вид.
- Обычная установка Bedrock Resource Pack не решала проблему.

### Решение

Исправленный Geyser mappings с настройкой `normalize: true` для свойства `damage`.

Это позволяет корректно сопоставлять значения повреждения Java-предметов с моделями Bedrock.

## Проверенная конфигурация

| Компонент | Версия |
|---|---|
| Paper | 1.21.10 |
| Geyser | 2.12.1-SNAPSHOT |
| MTVehicles | 2.5.8 |
| Java | 21 |
| Клиент | Minecraft Bedrock |

**Результат:** на проверенной конфигурации разные машины стали отображаться своими моделями.

## Установка

1. Установите оригинальный Bedrock Resource Pack от Tydium.
2. Скачайте исправленный mappings из этого репозитория.
3. Сделайте резервную копию старого mappings.
4. Поместите исправленный JSON в:

   `plugins/Geyser-Spigot/custom_mappings/`

5. Убедитесь, что Bedrock Resource Pack находится в:

   `plugins/Geyser-Spigot/packs/`

6. Перезапустите сервер и проверьте транспорт с Bedrock-клиента.

## Обновление для новых версий MTVehicles

Для новых версий MTVehicles сначала проверьте соответствие существующих моделей и текстур.

- Если модели и текстуры остались прежними, обычно достаточно обновить mappings под новые идентификаторы и значения предметов.
- Если появились новые машины или варианты транспорта, для них также потребуются соответствующие Bedrock-модели и текстуры.

Таким образом, не всегда достаточно просто заменить mappings.

## Важно

- Этот проект содержит исправление mappings, а не является официальным ресурс-паком MTVehicles.
- Оригинальные модели и текстуры принадлежат их авторам.
- Совместимость с другими версиями MTVehicles и Geyser не гарантируется.
- Перед обновлением сервера рекомендуется сохранить рабочие файлы.

## Благодарности

- **Tydium** — за оригинальный Bedrock-порт MTVehicles.
- **GeyserMC** — за возможность подключения Bedrock-клиентов к Java-серверам.

---

# English

## Description

A Geyser mappings compatibility fix for the MTVehicles resource pack on Minecraft Bedrock Edition.

This project is based on the unofficial Bedrock port by **Tydium**:

**Original project:** https://github.com/Tydium/MTVehicles-Bedrock-Pack

Many thanks to Tydium for the original work porting MTVehicles models and textures to Bedrock!

### The issue

When joining a Java server through Geyser using Bedrock Edition:
- Different vehicles could appear as the same model.
- Vehicle models and textures could display incorrectly.
- Installing the Bedrock resource pack alone did not solve the issue.

### The fix

A corrected Geyser mappings file using `normalize: true` for the `damage` property.

This allows Java item damage values to be mapped correctly to Bedrock models.

## Tested configuration

| Component | Version |
|---|---|
| Paper | 1.21.10 |
| Geyser | 2.12.1-SNAPSHOT |
| MTVehicles | 2.5.8 |
| Java | 21 |
| Client | Minecraft Bedrock |

**Result:** Different vehicles displayed their corresponding models in the tested configuration.

## Installation

1. Install the original Bedrock Resource Pack by Tydium.
2. Download the fixed mappings from this repository.
3. Back up your existing mappings.
4. Place the corrected JSON file in:

   `plugins/Geyser-Spigot/custom_mappings/`

5. Make sure the Bedrock Resource Pack is in:

   `plugins/Geyser-Spigot/packs/`

6. Restart the server and test vehicles using a Bedrock client.

## Updating for newer MTVehicles versions

For newer MTVehicles versions, first check whether the existing models and textures still match.

- If the models and textures have not changed, updating the mappings to match the new item identifiers and values is usually enough.
- If new vehicles or variants have been added, their corresponding Bedrock models and textures will also be needed.

Therefore, updating mappings alone is not always sufficient.

## Notes

- This project provides a mappings fix; it is not an official MTVehicles resource pack.
- Original models and textures belong to their respective authors.
- Compatibility with other MTVehicles and Geyser versions has not been verified.
- Always back up working files before updating your server.

## Credits

- **Tydium** — original MTVehicles Bedrock port.
- **GeyserMC** — Java-to-Bedrock cross-platform compatibility.
