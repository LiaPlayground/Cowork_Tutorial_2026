# Klassifikation der Teilnehmerfragen — Workshop 09.06.2026

> Interne Vorbereitungsnotiz. Grundlage: `LiaScript-Workshop_Fragensammlung.docx`
> (Sammlung der Teilnehmer:innen Christine, Christin, Heike, Silvia) und Abgleich
> mit der November-Einführung (CoP) *„LiaScript – Offene OER im Browser"*
> (<https://github.com/LiaPlayground/LiaScript-Offene-OER-im-Browser>, 30 min).

## 1. Wie wird klassifiziert?

Jede Frage wird entlang von **drei Dimensionen** eingeordnet:

| Dimension | Werte | Zweck |
| --------- | ----- | ----- |
| **A — Themencluster** | Features · Hintergrund/Betrieb · Struktur & Navigation · Medien · Design & Templates · Export & Nachnutzung · Erwartung/Format | Inhaltliche Gruppierung |
| **B — November-Abdeckung** | `🟢 angerissen` · `🟡 erwähnt, nicht vertieft` · `🔴 neu` | Was kannten die TN aus der 30-Min-CoP schon? → Fokus auf das, was dort zu kurz kam |
| **C — Workshop-Phase** | 01 Erleben · 02 Verstehen · 03 Anwenden · 04 Verbreiten · ⚠️ Lücke | Wo wird die Frage im aktuellen Material adressiert? |

**Lesart von B (November):** Die CoP war ein *Überblicksvortrag*, kein Praxis-Seminar
(mehrfach von TN angemerkt: „dafür war zu wenig Zeit", „ich war von einem
Einsteiger-Seminar ausgegangen"). Sie zeigte die *Bandbreite* (Feature-Landkarte,
Hosting-Optionen, Kollaboration, KI-Co-Creation, LMS-Vergleich, Export), aber nichts
*selbst gemacht*. Deshalb gilt: Auch `🟢 angerissen`-Themen sind im Workshop noch
offen — nur eben auf der *Anwendungs-*, nicht mehr auf der *Was-ist-das-Ebene*.

## 2. Klassifizierte Fragen

### Cluster: Features (über reines Markdown / HedgeDoc / CryptPad hinaus)

| # | Frage (TN) | B · Nov | C · Phase | Kommentar |
|---|------------|:------:|:--------:|-----------|
| F1 | „Zusätzliche Features, die über reines Markdown und Tools wie HedgeDoc/CryptPad hinausgehen" *(Christine)* | 🟢 | 01, 02 | Feature-Landkarte in Nov gezeigt; im Workshop in 01 *erlebt*, in 02 *systematisiert* (Abschnitt „Systematik hinter den Befehlen"). |
| F2 | „Besonders der KI-Assistent 🤖" *(Christine)* | 🟡 | 04 ⚠️ | Nov: Abschnitt 6 „KI-Co-Creation" + Beispiel-Prompt, aber nur als Konzept. **Lücke:** 04_Verbreiten behandelt KI bisher nicht praktisch. → Kandidat für Ausbau in Phase 04. |
| F3 | Tabellen über Markdown hinaus: Zellen verbinden, Zeilen/Spalten/Zellen einfärben *(Silvia)* | 🔴 | 03 ⚠️ | In Nov gar nicht. 01 zeigt `data-type="barchart"`-Tabelle, aber nicht Gestaltung. **Lücke / Cheatsheet-Kandidat.** |

### Cluster: Hintergrund & Betrieb

| # | Frage (TN) | B · Nov | C · Phase | Kommentar |
|---|------------|:------:|:--------:|-----------|
| F4 | „Was erfordert das Hosting? Was bedeutet das an Ressourcen für ein Hochschul-Rechenzentrum?" *(Christine)* | 🟡 | 04 ⚠️ | Nov nannte Hosting-*Optionen* (WebSpace, Git, IPFS, Data-URI), aber nicht die RZ-Ressourcen-Frage. **Kern-Botschaft:** kein Server nötig (läuft im Browser/statisches Hosting). → in 04 explizit adressieren. |

### Cluster: Struktur & Navigation

| # | Frage (TN) | B · Nov | C · Phase | Kommentar |
|---|------------|:------:|:--------:|-----------|
| F5 | Seiten/Kapitel untereinander verlinken *(Silvia)* | 🔴 | 03 ⚠️ | Nicht behandelt. **Lücke.** Cheatsheet-Thema (interne Links / Anker). |
| F6 | Vorhandene Seiten als **Wissensgraph** darstellen *(Silvia)* | 🔴 | ⚠️ | Nicht behandelt; technisch Spezialfall. → kurz einordnen (machbar via Plugin/Struktur), nicht überdehnen. |
| F7 | **Seitenleiste / Navigation anpassen** *(Silvia)* | 🔴 | 03 ⚠️ | Nicht behandelt. Hängt eng an Gliederung (`#`-Ebenen) + Makros. **Lücke**, relevant fürs Handbuch. |

### Cluster: Medien

| # | Frage (TN) | B · Nov | C · Phase | Kommentar |
|---|------------|:------:|:--------:|-----------|
| F8 | Bilder: Formate, Größenanpassung, Bildbeschreibung, Untertitel *(Silvia, Heike)* | 🟡 | 03 ⚠️ | Nov nutzte Bilder, erklärte sie nicht. **Anwenden-Thema** (alt-Text, `style=`-Größe). |
| F9 | **Audio** selbst aufgenommen einbinden *(Silvia, Christine)* | 🟡 | 03 ⚠️ | Nov: Text-to-Speech/Avatare ja, eigenes Audio nein. **Lücke.** |
| F10 | **Podcasts** aus externen Quellen (OERinfo u.a.) einbinden *(Silvia, Christine)* | 🔴 | 03/04 ⚠️ | Nicht behandelt. |
| F11 | **Video** — eigene (Hoch-/Querformat) + extern (YT, PeerTube, TIB-AV) *(Silvia)* | 🟢 | 01, 03 | Nov: Avatar-Videos + YT-Embeds. 01 bindet YT ein (`!?[]`). Format-/Quellenvielfalt noch praktisch zeigen. |
| F12 | **H5P**-Inhalte (interaktive Videos, Dialog Cards, Timeline) *(Silvia)* | 🔴 | 03/04 ⚠️ | Nicht behandelt. Wichtig: H5P-Einbindung + Abgrenzung zu nativen LiaScript-Quizzen. **Lücke.** |

### Cluster: Design & Templates

| # | Frage (TN) | B · Nov | C · Phase | Kommentar |
|---|------------|:------:|:--------:|-----------|
| F13 | **Templates** für Einheitlichkeit (viele Autor:innen am Handbuch) — wie funktionieren sie, wie gut einsetzen? *(Silvia, Christin, Christine)* | 🟢 | 03/04 ⚠️ | Nov: Abschnitt „Templates vs Plugins" (Video, `github.com/topics/liascript-template`) — nur benannt. **Hoher Bedarf, praktisch noch offen.** Zentrales Handbuch-Thema. |
| F14 | Gestaltungsoptionen / Design (Farben, Layout) — barrierearm, CC-BY-kompatibel; Co-WOERK-Wiedererkennung *(Silvia, Christine, Christin)* | 🟡 | 03/04 ⚠️ | Nov nur Demo-Optik. Hängt an `style.css` + Makros + Templates. Barrierefreiheit explizit gewünscht. |
| F15 | Strukturierung *innerhalb* einer Seite: Gliederung, Seitenindex *(Silvia)* | 🔴 | 03 ⚠️ | Verwandt mit F7. Nicht behandelt. |

### Cluster: Export & Nachnutzung

| # | Frage (TN) | B · Nov | C · Phase | Kommentar |
|---|------------|:------:|:--------:|-----------|
| F16 | **Export-Optionen** (PDF, andere Formate); Pandoc-Analogie aus Obsidian? Was bedeutet das für interaktive/multimediale Elemente? *(Silvia)* | 🟢 | 04 | Nov: Export-Tabelle (SCORM/PDF/IMS/Standalone/APK). 04 hat 5 Verbreitungswege. **Offene Teilfrage:** ehrliche Einschätzung, *was beim PDF-/Print-Export von Interaktivität verloren geht*. |
| F17 | LiaScript-Version als **SSoT** (Single Source of Truth) fürs Handbuch *(Silvia)* | 🟢 | 04 | Nov: Kernbotschaft „eine Textdatei, überall nutzbar". → in 04 als Arbeitsmodell fürs Handbuch festhalten. |
| F18 | Ehrliche **Aufwands-Einschätzung** für interaktive/multimediale Elemente *(Silvia)* | 🔴 | 03/04 ⚠️ | Nirgends adressiert. Wichtiger Vertrauens-Punkt — sollte ehrlich beantwortet werden. |

### Cluster: Erwartung & Format des Workshops (Meta)

| # | Aussage (TN) | B · Nov | C · Phase | Kommentar |
|---|--------------|:------:|:--------:|-----------|
| M1 | „Praxisorientierter Einstieg, damit ich am Handbuch mitarbeiten kann — in der CoP war zu wenig Zeit." *(Christin)* | — | alle | **Erwartungsabgleich:** Workshop ist als Hands-on (Phase 03, 70 min) angelegt → passt. |
| M2 | „Ich war von einem praxisorientierten Einsteiger-Seminar ausgegangen." *(Heike)* | — | alle | Wie M1. Eingangs kurz Erwartung framen: Nov = Überblick, heute = selber machen. |

## 3. Auswertung

### Was die November-CoP schon geleistet hat (→ heute nicht wiederholen, nur aufgreifen)
- Feature-*Bandbreite*, Hosting-Optionen, Kollaboration, **KI-Co-Creation (konzeptionell)**,
  LMS-Vergleich, Export-Formate (SCORM/PDF/IMS/Standalone). Alles auf **Überblicksebene**.

### Größte offene Lücken im aktuellen Workshop-Material (⚠️ = Handlungsbedarf)
1. **Templates** (F13) — meistgenannt, zentral fürs Handbuch, bisher nicht praktisch.
2. **KI-Assistent praktisch** (F2) — hohes Interesse, in 04 nur konzeptuell.
3. **Struktur/Navigation/Verlinkung** (F5, F7, F15) — Cluster, für Handbuch essenziell.
4. **Medien-Detailfragen** (F8–F12): eigenes Audio, Podcasts, H5P, Bild-Gestaltung.
5. **Tabellen-Gestaltung** (F3).
6. **Hosting/RZ-Ressourcen** (F4) und **Aufwands-Ehrlichkeit** (F18, F16-Teil).

### Bereits gut abgedeckt
- Quizformate, Code-Ausführung, Diagramme/Daten, Metadaten, YT-Video → **Phase 01** erlebbar.
- Grundphilosophie, Trennung Inhalt/Darstellung, Befehlssystematik → **Phase 02**.
- Verbreitungswege (Data-URI, ZIP, Git, SCORM, OPAL) → **Phase 04**.

### Empfehlung für Cheatsheet-Ergänzungen
Interne Links (F5), Tabellen-Gestaltung (F3), Bild-Optionen `style=`/alt-Text (F8),
Audio-Einbindung (F9) — alles kompakte Syntax, ideal fürs gedruckte Cheatsheet.
