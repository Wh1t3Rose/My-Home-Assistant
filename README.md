# My-Home-Assistant
Where I store my Home Assistant configs, including many shared on my blog: https://automateit.lol

## Included
- core/automations.yaml
- core/configuration.yaml
- cards/Cal-card.yaml
- cards/cat-card.yaml
- cards/Health-Cardyaml.yaml
- cards/Phone-Dash-Room_Card.yaml
- cards/timeline.yaml
- cards/navbar-card.yaml
- lovelace.yaml

## Recent Updates (2026-03-18)

### Cat Dashboard / Litter-Robot
- Updated `cards/cat-card.yaml` with safer numeric handling for weight cards.
- Switched weight trend display to 14-day stats sensors:
	- `sensor.marsh_weight_change_14d`
	- `sensor.max_weight_change_14d`
- Added a 14-day weight history graph to the cat popup.
- Updated litter box status text behavior:
	- Shows `Last Online: Now` while LR4 is online.
	- Shows `sensor.litter_robot_4_last_seen` value when LR4 is unavailable.

### Dashboard Sync
- Updated `dashboards/Phone-Dash.yaml` to match cat-card logic changes:
	- Trend cards use 14-day change sensors.
	- Litter box `Last Online` behavior mirrors cat-card.

### Core Config Updates
- Added 14-day statistics sensors in `core/configuration.yaml`:
	- `Marsh Weight Change 14d` from `sensor.marsh_weight_3`
	- `Max Weight Change 14d` from `sensor.max_weight_2`

### Notes
- This repo stores core files under `core/`:
	- local `automations.yaml` -> repo `core/automations.yaml`
	- local `configuration.yaml` -> repo `core/configuration.yaml`