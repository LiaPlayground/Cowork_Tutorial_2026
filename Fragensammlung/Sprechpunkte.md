# Sprechpunkte — alle Teilnehmerfragen abholen

> Leitfaden für die Moderation am 09.06.2026. Zu jeder Frage aus der
> [Klassifikation](Klassifikation.md): **was ansprechen**, ein **lauffähiges
> Beispiel** zum Vorzeigen (im Live-Editor) und der **Bezug zur Phase / zum Cheatsheet**.
>
> Syntax gegen die offizielle LiaScript-Doku geprüft (Stand 06/2026).
> Reihenfolge = Priorität: was im November zu kurz kam und fürs Handbuch zentral ist, zuerst.
>
> Legende: 🟢 in Nov-CoP angerissen · 🟡 erwähnt · 🔴 neu · ⚠️ aktuell Material-Lücke

---

## A. Templates — Einheitlichkeit fürs Handbuch *(F13 · 🟢 · ⚠️)*

**Ansprechen:** Wichtigste Frage. Templates sind keine „Designvorlagen" wie in Word,
sondern **importierte Markdown-Bausteine** (Makros, CSS, JS), die per `import:` im
YAML-Header eingebunden werden. Genau der Hebel für „alle Autor:innen, ein Look".
Abgrenzung Template (nachnutzbarer Baustein) vs. Plugin (Browser-Erweiterung) — in Nov nur benannt.

**Beispiel — gemeinsamer Look übers Handbuch:** ein zentrales Style-/Makro-Repo importieren:

```markdown
<!--
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/main/README.md
link:   https://raw.githubusercontent.com/Co-WOERK/handbuch-style/main/style.css
-->
```

Eigene Makros als wiederverwendbarer Baustein (z. B. ein einheitlicher Hinweis-Kasten):

```markdown
@infobox: <div class="cowoerk-info">@0</div>

@infobox(Dieser Baustein sieht in **jedem** Kapitel gleich aus.)
```

> **Botschaft:** Ein Style-Repo + ein Makro-Set = Single Source für das Design des ganzen
> Handbuchs. Jede:r Autor:in importiert dieselbe Zeile. Übersicht: `github.com/LiaTemplates`.
> **Bezug:** Cheatsheet S. 2 „LiaScript-Templates"; Phase 03/04.

---

## B. KI-Assistent praktisch *(F2 · 🟡 · ⚠️)*

**Ansprechen:** In Nov nur als Konzept gezeigt. Jetzt **live**: weil LiaScript reiner
Text ist, kann jede KI direkt LiaScript-Markdown erzeugen — kein Plattform-Lock-in.
Zwei Wege: (1) KI im Chat einen Kurs generieren lassen, (2) der **LiaScript-GPT/Assistent**.

**Beispiel — Prompt, der gültiges LiaScript liefert** (live im Editor einfügen):

```text
Erstelle einen kurzen LiaScript-Kurs zu "Boole'sche Operatoren in der OER-Recherche".
Nutze strikt LiaScript-Markdown: einen YAML-Header (author, language: de),
zwei Abschnitte mit `#`-Überschriften, je ein Quiz (Single-Choice mit [(X)]) und
einen Sprecher-Text mit --{{0}}--. Gib nur den Markdown-Code aus.
```

> **Ehrlich dazusagen:** KI ist gut für Struktur, Quiz-Entwürfe, Übersetzung, Umformulieren —
> **fachliche Korrektheit und Lizenzangaben** müssen Autor:innen prüfen. Co-Creation, kein Autopilot.
> **Bezug:** Phase 04 (Ausbau-Kandidat). Live-Demo > Folie.

---

## C. Struktur, Navigation & Verlinkung *(F5, F7, F15 · 🔴/🟡 · ⚠️)*

**Ansprechen:** Cluster, das fürs Handbuch (viele Kapitel) essenziell ist und in Nov fehlte.
Kernidee: **Die Seitenleiste/Navigation entsteht automatisch aus der Überschriften-Hierarchie.**
Man „baut" kein Menü — man strukturiert mit `#`, `##`, `###`.

**Beispiel — Navigation = Gliederung (F7, F15):**

```markdown
# Handbuch Kapitel 1        <!-- erscheint als oberster Navigationspunkt -->
## 1.1 Grundlagen           <!-- Unterpunkt -->
## 1.2 Lizenzen
### 1.2.1 CC-BY             <!-- noch eine Ebene tiefer -->
```

**Beispiel — Seiten/Kapitel untereinander verlinken (F5):** intern per `#` + Titel oder Foliennummer:

```markdown
Mehr dazu im [Lizenz-Kapitel](#1-2-lizenzen).

Springe zur [nächsten Folie](#15).
```

> **Hinweise zum Vorzeigen:** Anker = Überschrift kleingeschrieben, Leerzeichen→`-`.
> Klammern im Titel müssen kodiert werden (`(`→`%28`). Unter-Unter-Ebenen (`====`/`----`)
> tauchen *nicht* in der Navigation auf — bewusst zur Entzerrung nutzbar.
> **Wissensgraph (F6):** ehrlich — kein Out-of-the-box-Feature; machbar via eingebettetem
> Mermaid-Graph mit internen Links, aber kein Automatismus. Nicht überversprechen.

---

## D. Tabellen über Markdown hinaus *(F3 · 🔴 · ⚠️)*

**Ansprechen:** „Markdown-Tabellen sind simpel — geht mehr?" Ja: **Färben und Formatieren
per HTML-Kommentar**, sowohl für die ganze Tabelle als auch einzelne Zellen.
*Zellen verbinden (colspan/rowspan) gehört ehrlich zu den Grenzen* — dafür ggf. HTML-Tabelle.

**Beispiel — Tabelle + einzelne Zellen einfärben:**

```markdown
<!-- style="width: 60%; font-size: 14px" -->
| <!-- style="background: #E8F0E9" --> Operator | Wirkung      |
|:--------------------------------------------- |:------------ |
| <!-- style="background: #FDE8E8" --> AND       | verkleinert  |
| OR                                             | vergrößert   |
```

> **Plus:** Eine Tabelle wird mit `<!-- data-type="barchart" -->` direkt zum Diagramm
> (siehe Phase 01). **Grenze:** verbundene Zellen → reine HTML-`<table>` einbetten.
> **Bezug:** Cheatsheet S. 1 „Tabellen" (A5) + Diagramm-Hinweis.

---

## E. Medien — Bild, Audio, Video, Podcast, H5P *(F8–F12 · 🟡/🔴 · ⚠️)*

**Ansprechen:** Die meistgenannte Medien-Bandbreite. Eine zentrale Faustregel zeigen:
**`!` Bild · `?` Audio · `!?` abspielbares Medium · `??` eingebettete Ressource.**

**Beispiel — Bild mit Größe + Alt-Text (F8):**

```markdown
![Logo des Co-WOERK-Handbuchs](images/logo.png)<!-- style="width: 300px; border: 1px solid #ccc" -->
```

**Beispiel — eigenes Audio einbinden (F9):**

```markdown
?[Eigene Aufnahme: Einführung](media/intro.mp3 "Audio-Untertitel")
```

**Beispiel — Podcast aus externer Quelle / Video (F10, F11):**

```markdown
?[Podcast von OERinfo](https://soundcloud.com/.../episode)
!?[Erklärvideo (YouTube)](https://www.youtube.com/watch?v=VIDEO_ID)
!?[Eigenes Video, Hochformat](media/clip.mp4)
```

**Beispiel — H5P (F12) — ehrlich einordnen:** *Kein* offizielles H5P-Template.
Praktisch über iframe-Einbettung des H5P-Inhalts:

```markdown
??[Interaktives H5P-Video](https://app.lumi.education/run/XXXXXX)
```

> **Ehrlich dazusagen:** Native LiaScript-Quizze (S. 2, A12/A13) decken vieles ab, was man
> sonst mit H5P macht — und bleiben Teil der einen Textdatei. H5P bleibt extern eingebettet
> (Verfügbarkeit hängt am Host). Dialog Cards/Timeline ggf. nativ nachbauen.
> **Bezug:** Cheatsheet S. 2 „Medien abspielbar" (A9a) + „Eingebettete Ressource" (A9b).

---

## F. Design, Gestaltung & Barrierefreiheit *(F14 · 🟡 · ⚠️)*

**Ansprechen:** Gestaltung läuft über **`link:` (eigene CSS)** im Header + Klassen per
HTML-Kommentar — genau wie die `style.css` dieses Workshops. Wunsch explizit aufgreifen:
**barrierearm + CC-BY-kompatibel** (keine Lese-Hürden, guter Kontrast — vgl. Silvias Blog-Beispiel).

**Beispiel — eigenes Stylesheet + Klasse anwenden:**

```markdown
<!-- link: style.css -->

<!-- class="cowoerk-highlight" -->
> Dieser Kasten nutzt das Handbuch-Design aus der zentralen CSS.
```

> **Botschaft:** Design wird **einmal** in CSS/Template definiert (→ Punkt A) und überall
> wiederverwendet. Barrierefreiheit: Alt-Texte (Punkt E), Kontrast, keine reinen Farb-Codes.
> **Bezug:** `style.css` im Repo; Phase 03/04.

---

## G. Export, Aufwand & Hosting *(F16, F17, F18, F4 · 🟢/🟡/🔴)*

**Ansprechen:** Großteils in Phase 04 abgedeckt — hier die **offenen, ehrlichen** Teilfragen.

- **Export-Formate (F16):** SCORM 1.2/2004, IMS, PDF, Standalone-HTML, APK. Pandoc-Analogie:
  ja, Markdown ist Pandoc-fähig — aber für *interaktive* Elemente ist der **LiaScript-eigene
  Export** der Weg (Pandoc würde Interaktivität verlieren).
- **Was geht beim PDF/Print verloren? (ehrlich):** Quizze, ausführbarer Code, Animationen
  werden statisch — PDF ist Begleitmaterial, **nicht** die volle Erfahrung. → SSoT bleibt LiaScript (F17).
- **Aufwand (F18):** Text/Markdown sehr schnell; Aufwand steckt in *guten* Interaktionen,
  Mediengestaltung und Lizenzrecherche — nicht in der Technik. Realistisch benennen.
- **Hosting / RZ-Ressourcen (F4):** Kernbotschaft — **kein** Applikationsserver, keine DB.
  Statisches Hosting (GitHub Pages / beliebiger WebSpace) genügt; Rendering passiert im Browser
  der Lernenden. Für ein RZ also minimal.

```markdown
<!-- YAML-Header: Export & Verbreitung steuern -->
<!--
author: Co-WOERK Team
logo:   images/logo.png
-->
```

> **Bezug:** Phase 04 „Fünf Verbreitungswege" + „Export als SCORM". Hosting-Punkt dort ergänzen.

---

## H. Erwartungs-Framing zu Beginn *(M1, M2)*

**Gleich am Anfang (1 Minute) ansprechen**, um die Erwartung aus der Fragensammlung abzuholen:

> „Die November-CoP war der **Überblick** — was LiaScript *kann*. Heute machen wir es **selbst**:
> In Phase 3 (70 min) bauen Sie an einem echten Baustein fürs Handbuch. Alles, was Sie heute
> sehen, ist nachnutzbarer Text — Sie nehmen Vorlagen mit nach Hause."

> **Bezug:** rahmt M1 (Christin) und M2 (Heike) direkt; verknüpft mit Phase 03 Hands-on.

---

## Checkliste — habe ich alle abgeholt?

| Frage | Punkt | Erledigt im Workshop |
|------|:-----:|:--------------------:|
| F1 Features über Markdown hinaus | A,E (+ Phase 01/02) | ☐ |
| F2 KI-Assistent | **B** | ☐ |
| F3 Tabellen (färben/verbinden) | **D** | ☐ |
| F4 Hosting / RZ-Ressourcen | **G** | ☐ |
| F5 Seiten verlinken | **C** | ☐ |
| F6 Wissensgraph | C (ehrlich begrenzt) | ☐ |
| F7 Seitenleiste / Navigation | **C** | ☐ |
| F8 Bilder (Größe, Alt, Untertitel) | **E** | ☐ |
| F9 Eigenes Audio | **E** | ☐ |
| F10 Podcasts extern | **E** | ☐ |
| F11 Video (Formate, Quellen) | E (+ Phase 01) | ☐ |
| F12 H5P | **E** (ehrlich) | ☐ |
| F13 Templates | **A** | ☐ |
| F14 Design / Barrierefreiheit | **F** | ☐ |
| F15 Gliederung auf Seite / Index | **C** | ☐ |
| F16 Export-Optionen / Pandoc | G (+ Phase 04) | ☐ |
| F17 SSoT Handbuch | G (+ Phase 04) | ☐ |
| F18 Aufwands-Einschätzung | **G** | ☐ |
| M1/M2 Erwartung Einsteiger-Praxis | **H** | ☐ |
