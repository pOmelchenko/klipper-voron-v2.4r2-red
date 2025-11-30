# Changelog

## 2025-12-01
- CANCEL_PRINT now skips SDCARD_RESET_FILE while a virtual SD print is still active and surfaces a console notice instead.
- Probe re-tuned; updated `z_offset` from -0.760 to -0.960 in the saved config block.

## 2025-11-28
- Docs split into EN/RU with CB2 hardware noted.
- Moonraker hardened: channel set to stable, trusted_clients narrowed to 192.168.1.0/24, CORS trimmed.
- Motion: lowered Z max speed.
- Macros: CANCEL_PRINT now lifts Z within remaining travel and parks XY only when homed.

## 2025-11-27
- Chamber soak macros: clearer responses and fan handling; simplified messaging.
- PAUSE macro: clarified comments and safeguards for parking/retraction.
- Changelog process: auto-generated seed, regrouped by date, and merged workflow changes.

## 2025-11-24
- Minor printer parameter touch-ups.

## 2025-11-17
- Major printer.cfg rewrite: structured sections, updated limits, clearer annotations.

## 2025-11-04
- Printer configuration rebalance with multiple parameter updates/removals.

## 2025-10-27
- Added Moonraker options and small printer adjustments.

## 2025-10-20
- Overhauled Moonraker auth/update-manager; large refactor of printer module layout.
- Removed chopper tuning file, menus, and macro suite to simplify configuration.

## 2024-12-25
- Added `chopper_tune.cfg`, refreshed macros/menus/Moonraker, and slimmed printer settings.

## 2024-07-21
- Added cached G28 macro; refreshed menus and Moonraker; substantial printer.cfg updates.

## 2024-04-27
- Further tuning of motion/heater sections in printer configuration.

## 2024-04-26
- Updated Moonraker settings and printer parameters for the current setup.

## 2024-04-15
- Removed unused print lifecycle macros; minor configuration tweaks.

## 2024-03-16
- Moved configs to `config/`, pruned KAMP, simplified includes and print start macro.

## 2024-02-28
- Added head light toggle/reset macros and surfaced them in menus.

## 2024-01-20
- Updated KAMP settings and small printer-side adjustments.

## 2024-01-09
- Follow-up printer parameter corrections.

## 2024-01-08
- Cleaned macros (removed move-to-center; adjusted nozzle clean/end); retuned several parameters.

## 2023-08-31
- Split chamber sensors (head/back), switched X/Y to physical endstops, reduced stepper currents to 0.80A; pin and TAP calibration tweaks.

## 2023-08-11
- Retuned drivers: lowered extruder current; raised X/Y/Z to 1.13A.

## 2023-07-29
- Added dump-variables and nozzle cleaning macros; refreshed Moonraker and printer settings.

## 2023-07-26
- Added KAMP and move-to-center helper; tweaked print start flow and aligned config.

## 2023-07-16
- Initial drop: printer settings, Moonraker config, menus, and start/pause/resume/end/cancel macros plus speed test routines.
