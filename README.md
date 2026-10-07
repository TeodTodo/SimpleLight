# SimpleLight

Home Assistant automation blueprint for the Philips Hue Dimmer Switch (Hue integration or Zigbee2MQTT).

| Button | Press | Hold |
|---|---|---|
| 1 | On / off (warm white; Hue lights get Hue "Bright") | — |
| 2 | One step brighter | Smooth ramp up until release |
| 3 | One step dimmer | Smooth ramp down until release |
| 4 | Next enabled color from a configurable list (cycles) | — |

Zigbee2MQTT groups are detected automatically from the selected lights / area. After switching on, every group lamp's real state is read back and lamps that missed the command are corrected (up to five rounds).

## Install

[![Open your Home Assistant instance and show the blueprint import dialog.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FTeodTodo%2FSimpleLight%2Fblob%2Fmain%2Fblueprints%2Fautomation%2FSimpleLight.yaml)

Or import this URL in **Settings → Automations & Scenes → Blueprints → Import Blueprint**:

```
https://github.com/TeodTodo/SimpleLight/blob/main/blueprints/automation/SimpleLight.yaml
```

## Updating

`main` is the released version. To pick up changes in Home Assistant, open **Blueprints**, then **⋮ → Re-import blueprint** on SimpleLight.

New features are developed on `feature/*` branches and merged into `main` through a pull request.

Input keys are part of the public interface: existing automations reference them by name. Add new inputs (with a `default:`) instead of renaming or removing old ones.
