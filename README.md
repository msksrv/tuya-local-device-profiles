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

### Energy monitoring SY2 (AT-Q-SY2-JWT)

Local Tuya profile for the SY2 DIN-rail energy monitoring device with relay control.

**Also sold / referenced as:**
- **TO-Q-SY2-JWT** (Tongou branding)
- **TQ-SY2-JWT** (alternative)

**Model identifier reported by the device:** **AT-Q-SY2-JWT**

#### Features
- Relay control (on/off)
- Energy monitoring:
  - Total Energy (kWh, `total_increasing`, compatible with HA Energy dashboard)
  - Power (W), Voltage (V), Current (mA)
- Fault detection via DP26 bitfield:
  - Individual fault flags (over current / over voltage / over power / low current / under voltage / under power)
  - Aggregated **“Fault (Any)”** sensor
- Read-only calibration coefficients (voltage / current / power / energy)
- Device configuration:
  - Power-on behavior (off / on / last state)
  - LED / indicator mode
  - Child lock
- Internal temperature sensor (diagnostic)
- Full alarm configuration via structured DP48 / DP49 records:
  - High temperature
  - High power
  - Overcurrent
  - Overvoltage
  - Undervoltage
- Online state query selector (DP66)
- Fully local operation (no Tuya Cloud required)

**Keywords:** AT-Q-SY2-JWT, TO-Q-SY2-JWT, TQ-SY2-JWT, SY2 energy monitor, Tuya DIN rail meter

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

### Energy monitoring SY2 (AT-Q-SY2-JWT) — RU

Локальный профиль Tuya для DIN-модуля мониторинга энергии серии SY2 с управлением реле.

**Также продаётся / встречается как:**
- **TO-Q-SY2-JWT** (бренд Tongou)
- **TQ-SY2-JWT** (альтернативные)

**Фактическая модель, возвращаемая устройством:** **AT-Q-SY2-JWT**

#### Возможности
- Управление реле (вкл / выкл)
- Мониторинг энергии:
  - Общая энергия (кВт·ч, `total_increasing`, совместимо с Energy Dashboard Home Assistant)
  - Мощность (Вт), Напряжение (В), Ток (мА)
- Обработка аварий через битовую маску DP26:
  - Отдельные флаги аварий (переток / перенапряжение / перегрузка / низкий ток / пониженное напряжение / низкая мощность)
  - Сводный сенсор **«Fault (Any)»**
- Диагностические коэффициенты калибровки (напряжение / ток / мощность / энергия, только чтение)
- Настройки устройства:
  - Поведение при включении питания (выкл / вкл / последнее состояние)
  - Режим индикатора / LED
  - Детский замок
- Встроенный датчик температуры (диагностика)
- Полная настройка аварий через структурированные записи DP48 / DP49:
  - Перегрев
  - Превышение мощности
  - Переток
  - Перенапряжение
  - Пониженное напряжение
- Запрос состояния online_state (DP66)
- Полностью локальная работа (без облака Tuya)

**Ключевые слова:** AT-Q-SY2-JWT, TO-Q-SY2-JWT, TQ-SY2-JWT, SY2 монитор энергии, Tuya DIN-модуль  

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

