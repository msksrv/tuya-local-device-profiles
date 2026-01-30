# tuya-local-device-profiles
Custom Tuya Local device profiles and extensions not accepted upstream
# Tuya Local – Custom Device Profiles

This repository contains **custom Tuya Local device profiles** and extensions that are not available upstream.

The profiles here:
- use **only locally available DPS**
- require **no changes to Tuya Local integration code**
- are tested with **local Tuya protocol** (no cloud dependency)
- extend device functionality where upstream profiles are minimal

## Currently included devices

### GEYA ZN03 Smart Breaker (single-phase)

Adds full local configuration of voltage protection logic:
- Overvoltage / Undervoltage thresholds
- Protection delays
- Selectable protection actions: **Disabled / Alarm / Trip**

## Installation

1. Copy the desired YAML file into:
   custom_components/tuya_local/devices/
3. Restart Home Assistant
4. Reconfigure the device if needed

## Notes

These profiles follow the existing Tuya Local device YAML format.  
They are maintained separately to avoid impacting upstream maintenance policy.

Upstream context: https://github.com/make-all/tuya-local/issues/4413


## Disclaimer

This is **not an official Tuya Local repository**.  
Use at your own discretion.


---

# Tuya Local – Пользовательские профили устройств

Этот репозиторий содержит **пользовательские профили устройств для Tuya Local** и расширения, которые отсутствуют в основном репозитории.

Профили в этом репозитории:
- используют **только локально доступные DPS**
- **не требуют изменений кода** интеграции Tuya Local
- работают через **локальный протокол Tuya** (без облака)
- расширяют функциональность устройств, где upstream-профили минимальны

## Поддерживаемые устройства

### GEYA ZN03 Smart Breaker (однофазный)

Добавляет полную локальную настройку логики защиты по напряжению:
- Пороги повышенного и пониженного напряжения
- Задержки срабатывания защит
- Выбор действия защиты: **Отключено / Тревога / Отключение**

## Установка

1. Скопируйте нужный YAML-файл в каталог:
   custom_components/tuya_local/devices/

2. Перезапустите Home Assistant
3. При необходимости заново настройте устройство

## Примечания

Профили соответствуют существующему формату YAML Tuya Local.  
Они поддерживаются отдельно, чтобы не влиять на политику сопровождения основного репозитория.

Upstream context: https://github.com/make-all/tuya-local/issues/4413

## Отказ от ответственности

Это **неофициальный репозиторий Tuya Local**.  
Используйте на свой страх и риск.

