# Changelog

## 2023-07-16 — cb0b361
- Initial configuration drop with printer settings, Moonraker config, menus, and print lifecycle macros (start/pause/resume/end/cancel) alongside speed test routines. 

## 2023-07-26 — 00f4fc8
- Added KAMP settings and move-to-center helper macro, tweaked print start flow, and aligned printer configuration with the new macros.

## 2023-07-29 — 7cd8946
- Introduced dump-variables and nozzle cleaning macros, refreshed Moonraker configuration, and adjusted printer settings accordingly.

## 2023-08-11 — 56bd282
- Retuned stepper drivers: lowered extruder current and increased run currents on X/Y/Z to 1.13A for improved motion control.

## 2023-08-31 — 9f02d6f
- Split chamber temperature sensing to separate head/back sensors, switched X/Y to physical endstops, and reduced stepper run currents to 0.80A.

## 2023-08-31 — 1bb9694
- Minor printer configuration tweak following the endstop and current adjustments.

## 2023-08-31 — fdc6271
- Updated printer pinning to match the changed head PCB wiring.

## 2023-08-31 — bff5299
- Reworked TAP probe calibration parameters and related motion settings in printer configuration.

## 2024-01-08 — 85b075a
- Cleaned up macros (removed move-to-center, adjusted nozzle clean and print end) and retuned multiple printer parameters.

## 2024-01-09 — a515d10
- Follow-up printer tuning with additional parameter corrections.

## 2024-01-20 — 6d7bc52
- Updated KAMP settings and applied small printer-side adjustments.

## 2024-02-28 — 4b47ef1
- Added head light toggle/reset macros and reorganized menu entries to surface the new lighting controls.

## 2024-03-16 — 0bb7827
- Relocated configuration from `klipper_config/` to `config/`, pruned KAMP settings, and simplified includes and print start macro.

## 2024-04-15 — 4d110f3
- Removed unused print lifecycle macros and made minor printer configuration tweaks.

## 2024-04-26 — b9c4bd9
- Added Moonraker settings and adjusted printer parameters for the latest setup.

## 2024-04-27 — 5e6370e
- Further printer configuration tuning across motion and heater sections.

## 2024-07-21 — ff14c2a
- Added cached G28 macro, refreshed menus and Moonraker configuration, and applied substantial printer configuration updates.

## 2024-12-25 — 10785fc
- Added `chopper_tune.cfg`, updated macros/menus/Moonraker, and slimmed down printer settings.

## 2025-10-20 — cec424c
- Removed chopper tuning file, menus, and the macro suite, trimming the configuration set considerably.

## 2025-10-20 — a015469
- Major Moonraker authorization and update-manager overhaul plus a large rewrite of printer configuration layout and modules.

## 2025-10-27 — 5c33746
- Added new Moonraker options and minor printer adjustments.

## 2025-11-04 — c2df591
- Significant printer configuration rebalance with many parameter updates and removals.

## 2025-11-17 — 467c526
- Comprehensive printer.cfg rewrite with structured sections, updated limits, and clearer annotations.

## 2025-11-24 — 82fff38
- Small follow-up printer parameter tweaks.

## 2025-11-27 — 4eb63d0
- Improved chamber temperature soak macros with clearer responses and fan control steps.

## 2025-11-27 — c63736a
- Simplified chamber soak macro messaging while keeping fan behavior intact.

## 2025-11-27 — 6ec11c4
- Updated pause macro comments and safeguards, clarifying parking and retraction logic.
