# Home Assistant blueprints

🇬🇧 English · 🇳🇱 [Nederlands](README.nl.md)

Home Assistant blueprints by Fliha. Each blueprint is available in English and Dutch.

## TV program starting soon

| Language | Import |
| --- | --- |
| 🇬🇧 English | [![Import blueprint into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FFliha%2Fha-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Ftv_program_notification.yaml) |
| 🇳🇱 Nederlands | [![Importeer blueprint in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FFliha%2Fha-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Ftv_programma_melding.yaml) |

Sends a notification (and optionally runs extra actions) a number of minutes before a TV program starts. The start time is looked up automatically in the TV guide.

**Requires:** the [EPG integration](https://github.com/yohaybn/HA_EPG) (open-epg.com), which creates one sensor per channel. The channel field only shows sensors from that integration.

**Settings**

| Field | Description |
| --- | --- |
| Channel | The EPG sensor of the channel |
| Program name | (Part of) the title, case-insensitive |
| Minutes in advance | Default 5 |
| Only if it starts after / and before | Time window, e.g. to skip repeats at night. 00:00 to 00:00 = whole day |
| Notify | One or more notify entities |
| Title / Message | Available variables: `{{ program }}`, `{{ channel }}`, `{{ start_time }}`, `{{ minutes }}`, `{{ description }}` |
| Extra actions | E.g. turn on the TV or a spoken announcement |

Files: [`tv_program_notification.yaml`](blueprints/automation/tv_program_notification.yaml) (English) · [`tv_programma_melding.yaml`](blueprints/automation/tv_programma_melding.yaml) (Dutch)

## License

[MIT](LICENSE)
