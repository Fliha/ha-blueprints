# Home Assistant blueprints

Blueprints van Fliha voor Home Assistant.

## TV-programma begint binnenkort

[![Importeer blueprint in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FFliha%2Fha-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Ftv_programma_melding.yaml)

Stuurt een melding (en voert eventueel extra acties uit) een aantal minuten voordat een tv-programma begint. De begintijd wordt automatisch opgezocht in de tv-gids.

**Vereist:** de [EPG-integratie](https://github.com/yohaybn/HA_EPG) (open-epg.com) met een sensor per zender. In het zenderveld zie je alleen sensoren van die integratie.

**Instellingen**

| Veld | Uitleg |
| --- | --- |
| Zender | De EPG-sensor van de zender, bijv. SBS6 |
| Programmanaam | (Een deel van) de titel, hoofdletters maken niet uit |
| Minuten van tevoren | Standaard 5 |
| Alleen als het begint na / en vóór | Tijdvenster, bijv. om nachtelijke herhalingen over te slaan. 00:00 tot 00:00 = hele dag |
| Melding naar | Eén of meer notify-entiteiten |
| Titel / Bericht | Te gebruiken variabelen: `{{ programma }}`, `{{ zender }}`, `{{ starttijd }}`, `{{ minuten }}`, `{{ omschrijving }}` |
| Extra acties | Bijv. tv aanzetten of een gesproken melding |

Bestand: [`blueprints/automation/tv_programma_melding.yaml`](blueprints/automation/tv_programma_melding.yaml)
