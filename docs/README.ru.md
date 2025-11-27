# Конфигурация (Voron 2.4r — Manta M8P + SB2040)

Кратко: где лежат файлы, под какое железо/макросы, как применить и проверить. Историю изменений смотрите в `CHANGELOG.md`.

## Пути
- Основной каталог: `~/klipper_config`
- Альтернатива (симлинк): `~/printer_data/config`
- Заливать из репозитория: `config/printer.cfg`, `config/moonraker.conf`

## Аппаратная база
- Плата: BTT Manta M8P v1.1 + CB2
- Хотэнд/инструмент: Mellow SB2040 PRO V3 (CAN)
- Кинематика: CoreXY, 4 Z-мотора (QGL), рама Voron 2.4r
- Интерфейс: mini12864, неопиксели на голове и панели

## Что настроено
- Макросы START/END/PAUSE/RESUME с QGL, bed mesh и Nevermore.
- Безопасный `CANCEL_PRINT`: поднимает Z в доступный остаток хода и паркует XY только при хоуме.
- Входной шейпинг через LIS2DW на голове.
- Moonraker на канале `stable`, `trusted_clients` сужены до `192.168.1.0/24`.

## Как применить
1) Скопировать `config/printer.cfg` и `config/moonraker.conf` в активный каталог выше.
2) Перезапустить службы или применить через UI:
```shell
sudo service klipper restart
sudo service moonraker restart
```
3) В веб-интерфейсе убедиться, что ошибок нет.

## Быстрые проверки
- `RESTART` в консоли Klipper проходит без ошибок.
- `STATUS` показывает MCU, движки, датчики и вентиляторы.
- Холостой `CANCEL_PRINT`: Z поднимается, XY паркуется, лимиты не срабатывают.

## Примечания
- При смене сети обновите `trusted_clients` в `moonraker.conf`.
- Для теста dev-обновлений вручную переключайте `channel` на `dev` и держите возможность отката.
