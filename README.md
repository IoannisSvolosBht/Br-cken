# Berlin Bridge Dashboard :bridge_at_night:

**Webanwendung zur Analyse und Priorisierung von Brückeninfrastruktur in Berlin**  
*Entwickelt für die Senatsverwaltung für Verkehr, Stadtentwicklung und Klimaschutz*

---

## :dart: Zweck
Diese **R/Shiny-Anwendung** visualisiert den Zustand, die Verkehrslast und den Sanierungsbedarf von Brücken in Berlin. Sie dient als Entscheidungshilfe für:
- **Verkehrsplanung** (Umleitungen, Kapazitätsanalysen)
- **Investitionspriorisierung** (Sanierungsbedarf nach Dringlichkeit)
- **Risikomanagement** (Hochwassergefährdete Brücken)

---

## :mag: Kernfunktionen
### 1. Interaktive Karte
- **Filterung** nach Bezirk, Baujahr, Zustand (gut/mangelhaft/kritisch)
- **Echtzeit-Analysen**: Verkehrsaufkommen, Schadensklassen
- **Tooltips** mit Brückenmetadaten (Letzte Inspektion, Traglast)

### 2. Priorisierungs-Dashboard
- **Top 10 Sanierungskandidaten** nach:
  - Baujahr (> 50 Jahre)
  - Verkehrsbelastung (DTV > 10.000 KFZ/Tag)
  - Zustandsnote (< 3.0)

### 3. Automatisierte Berichte
- PDF-Export für Sitzungsvorlagen
- GeoJSON-Export für GIS-Systeme

---

## :computer: Technischer Stack
- **Backend**: R (v4.3+) mit `sf`, `leaflet`, `shiny`
- **Datenquellen**:
  - Amtliche Brückendaten (FIS-Broker Berlin)
  - Echtzeit-Verkehrsdaten (SenUVK)
- **Hosting**: Docker-Container auf AWS (für Behörden-Intranet)

---

## :rocket: Schnellstart
1. **Anwendung testen** (Demo):
   ```bash
   docker run -p 3838:3838 ghcr.io/ihrrepo/berlin-bridges:latest
    
