D&D RANDOM TABLES V2
====================

INHOUD
- index.html                 De complete app (HTML, CSS en JavaScript)
- manifest.webmanifest       PWA-installatiegegevens
- sw.js                      Offline cache / service worker
- icon.svg                   App-icoon

SNEL STARTEN
1. Upload alle bestanden uit deze map naar de root van je GitHub Pages-repository.
2. Commit en push de wijzigingen.
3. Open de GitHub Pages-URL in Chrome op Android terwijl je online bent.
4. Kies in Chrome-menu eventueel 'App installeren' of 'Toevoegen aan startscherm'.

GEBRUIK
- Roll: kies een tabel, stel het aantal worpen in en rol. Gewone tabellen geven iedere niet-lege entry een gelijke kans.
- Weather: gebruikt drie onafhankelijke d6 en telt de ogen op. De totalen 3 t/m 18 wijzen naar entries 1 t/m 16.
- Location: kiest willekeurig een History-, Featured- en Inhabitant-tabel en rolt op elk.
- NPC / Roll20: rolt de twee NPC-sets. De Roll20-macro's zijn exact opgenomen en hebben kopieerknoppen.
- Tables: voeg tabellen en entries toe, bewerk ze of verwijder ze. De negen Location-tabellen, Weather, Loot en de negen NPC-tabellen zijn vooraf aangemaakt.
- Saved: bewaar individuele resultaten en verwijder ze later.
- Data: exporteer of importeer een JSON-back-up.

GEGEVENS EN MIGRATIE
- Nieuwe gegevens staan in localStorage onder: dnd-random-tables-v2
- Bij de eerste start probeert V2 automatisch dnd-random-tables-v1 te lezen.
- De V1-sleutel wordt niet verwijderd. V2 schrijft de geconverteerde data pas weg nadat het lezen en normaliseren is gelukt.
- Maak voor de zekerheid altijd zelf eerst een JSON-export van V1 als die app nog toegankelijk is.
- Importeren vervangt de huidige V2-data; exporteer eerst om overschrijven te voorkomen.

UPDATES
- De service worker gebruikt cacheversie dnd-random-tables-v2-cache-1.
- Verhoog het getal achter 'cache-' in sw.js bij een volgende release.
- Na een update kan Chrome de nieuwe service worker installeren bij een bezoek. Sluit/heropen de PWA of vernieuw de pagina als de oude versie nog zichtbaar is.

OPMERKINGEN
- Gegevens worden lokaal in de browser van dit apparaat bewaard. Wis de sitegegevens van Chrome niet zonder eerst een back-up te exporteren.
- Offline gebruik werkt nadat de app minimaal één keer online is geopend en de service worker de bestanden heeft gecachet.
- De app heeft geen directe verbinding met Roll20; NPC-tabellen zijn lokale kopieën.
- GitHub Pages levert de site via HTTPS, wat vereist is voor PWA-service workers.
