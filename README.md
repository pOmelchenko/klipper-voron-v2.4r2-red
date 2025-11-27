# Configuration Overview (Voron 2.4r — Manta M8P + SB2040)

Concise reference for where configs live, what hardware/flows they target, and how to deploy/check them. See `CHANGELOG.md` for a dated change history. Russian version: `docs/README.ru.md`.

## Paths
- Primary: `~/klipper_config`
- Symlinked alternative: `~/printer_data/config`
- Repo files to deploy: `config/printer.cfg`, `config/moonraker.conf`

## Hardware snapshot
- Controller: BTT Manta M8P v1.1 + CB2
- Toolhead: Mellow SB2040 PRO V3 (CAN)
- Mechanics: CoreXY, quad Z (QGL), Voron 2.4r frame
- UI/lighting: mini12864, neopixels on head and panel

## What’s configured
- Print lifecycle macros (START/END/PAUSE/RESUME) with QGL, bed mesh, and Nevermore handling.
- Safe `CANCEL_PRINT`: raises Z within remaining travel and parks XY only when homed.
- Input shaping via LIS2DW on the toolhead.
- Moonraker locked to `channel: stable`, trusted clients narrowed to `192.168.1.0/24`.

## Deploy
1) Copy `config/printer.cfg` and `config/moonraker.conf` into the active config dir above.
2) Restart services or apply via UI:
```shell
sudo service klipper restart
sudo service moonraker restart
```
3) Open the web UI, confirm there are no config errors.

## Quick validation
- `RESTART` in the Klipper console completes without errors.
- `STATUS` shows MCUs, steppers, sensors, and fans present.
- Dry-run `CANCEL_PRINT`: Z lifts, XY parks, no limit errors.

## Notes
- For a network change, update `trusted_clients` in `moonraker.conf` accordingly.
- For bleeding-edge updates, switch `channel` to `dev` manually and be ready to revert.
