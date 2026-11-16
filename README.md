# MTVehicles-Geyser-Bedrock-Fix
MTVehicles compatibility fix for Geyser Bedrock
# MTVehicles — Geyser Bedrock Compatibility Fix

**Русский | [English below](#english)**

## Описание

Исправление совместимости ресурспака MTVehicles с Bedrock Edition через Geyser.

### Проблема

При подключении к Java-серверу через Bedrock:
- Разные машины могли отображаться одной и той же моделью.
- Транспорт мог иметь неправильные текстуры или внешний вид.
- Обычная установка Bedrock Resource Pack не решала проблему.

### Решение

Исправленный файл Geyser mappings с настройкой `normalize: true` для свойства `damage`.

Это позволяет корректно сопоставлять значения повреждения предметов Java с моделями Bedrock.

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

1. Остановите Minecraft-сервер.
2. Сделайте резервную копию старого mappings-файла.
3. Поместите исправленный JSON в папку:

   `plugins/Geyser-Spigot/custom_mappings/`

4. Оставьте соответствующий Bedrock Resource Pack в папке:

   `plugins/Geyser-Spigot/packs/`

5. Запустите сервер.
6. Переподключитесь с Bedrock-клиента и проверьте несколько разных машин.

## Важно

- Этот проект содержит исправление mappings, а не полный ресурспак MTVehicles.
- Для работы необходим совместимый Bedrock Resource Pack.
- Совместимость с другими версиями MTVehicles и Geyser не гарантируется.
- Перед обновлением сервера рекомендуется сохранить рабочие файлы.

## Благодарности

Спасибо разработчикам MTVehicles и Geyser за их проекты.

---

<a name="english"></a>
# English

## Description

A Geyser mappings compatibility fix for the MTVehicles resource pack on Minecraft Bedrock Edition.

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

1. Stop your Minecraft server.
2. Back up your existing mappings file.
3. Place the corrected JSON file in:

   `plugins/Geyser-Spigot/custom_mappings/`

4. Keep the compatible Bedrock Resource Pack in:

   `plugins/Geyser-Spigot/packs/`

5. Start the server.
6. Reconnect using a Bedrock client and test several vehicles.

## Notes

- This project provides a mappings fix, not the original MTVehicles resource pack.
- A compatible Bedrock Resource Pack is required.
- Compatibility with other MTVehicles and Geyser versions has not been verified.
- Always back up working files before updating your server.

## Credits

Thanks to the developers of MTVehicles and Geyser.
