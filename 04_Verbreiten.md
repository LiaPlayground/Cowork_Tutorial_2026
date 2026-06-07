<!--
author:   Sebastian Zug, André Dietrich

email:    sebastian.zug@informatik.tu-freiberg.de

version:  0.1.0

language: de

narrator: Deutsch Male

mode:     Presentation

date:     09/06/2026

comment:  Phase 4 des Workshops "Interaktive OER mit LiaScript erstellen" (Potsdam, 09.06.2026).
          Verbreiten und Disseminierung eigener Kurse - 15 Minuten.

repository: https://github.com/LiaPlayground/Cowork_Tutorial_2026

attribute: Interaktive OER mit LiaScript erstellen
           von Sebastian Zug und André Dietrich
           ist lizenziert unter [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

link:     style.css

-->

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/Cowork_Tutorial_2026/main/04_Verbreiten.md)

# Verbreiten von LiaScript-Kursen

> <h2>Phase 4 des Workshops "Interaktive OER mit LiaScript erstellen"</h2>
>
> <div style="height: 2.5em;"></div>
>
> <h4>Prof. Dr. Sebastian Zug, TU Bergakademie Freiberg</h4>
> <h4>Dr. André Dietrich, TU Bergakademie Freiberg</h4>
>
> <h4>09.06.2026</h4>

--------------------------------------------

## Worum geht es in diesen 15 Minuten?

Sie haben in Phase 3 ("Anwenden") Ihren eigenen Kurs gebaut — jetzt geht es darum, ihn aus dem LiveEditor herauszubekommen und mit anderen zu teilen. Konkret klären wir:

- Wie kommt Ihr Kurs aus dem LiveEditor zu einer Kollegin in einem anderen Haus?
- Welcher Weg passt zu welchem Szenario — schnelle Vorschau, vollständiger Kurs, LMS-Integration?
- Was bleibt von den 5V-Freiheiten in jedem Verbreitungsweg erhalten?

> [!NOTE]
> Viele der Schritte, die Sie in Phase 3 selbst durchgeführt haben, übernehmen in entsprechenden Editoren KIs. Das heißt: Sie müssen nicht mehr wissen, *wie* man Markdown schreibt, um einen interaktiven Kurs zu erstellen. Sie müssen nur noch wissen, *was* Sie vermitteln wollen — und die KI erledigt den Rest.

## Teil A — KI als Co-Autorin für LiaScript-Kurse

Vor zwei Jahren hieß die Antwort auf „Wie schreibe ich einen LiaScript-Kurs?" noch: *„Cheat Sheet öffnen, Syntax nachschlagen, ausprobieren."* Heute heißt sie zunehmend: *„Beschreiben Sie der KI, was Sie unterrichten wollen — und prüfen Sie die Vorlage."*

> [!NOTE]
> **Was sich nicht geändert hat:** Die Lehrkraft entscheidet, *was* unterrichtet wird, *welches Beispiel* gewählt wird, *welche Differenzierung* sinnvoll ist. Die KI nimmt nur die **Syntax-Last** ab — sie weiß, wie ein Quiz, eine Formel oder eine Animation in LiaScript geschrieben werden.

### Professionelle Editierung

Der LiveEditor ist ein großartiges Werkzeug, um die Möglichkeiten von LiaScript kennenzulernen und erste Kurse zu bauen. Aber er ist nicht der einzige Weg, um einen Kurs zu erstellen. 

* Visual Studio Code mit GitHub Copilot bietet eine professionelle Umgebung, um Kurse zu entwickeln — mit Syntax-Highlighting, Versionskontrolle und KI-Unterstützung.
* Github Codespaces ermöglicht es, direkt im Browser an Kursen zu arbeiten, ohne eine lokale Entwicklungsumgebung einrichten zu müssen.
* ...

### Zwei Stufen der KI-Nutzung

           {{0-1}}
**************************************

**Stufe 1 — Web-KI mit angehängter Skill-Datei**

Die niedrigschwellige Variante: Eine einzige Markdown-Datei, [**LiaSkill**](https://github.com/LiaScript/LiaSkill), wird einer Web-KI als Kontext mitgegeben — Claude, ChatGPT, Gemini oder Mistral, egal welche. Die KI „lernt" daraus die vollständige LiaScript-Syntax und kann anschließend komplette Kurse aus Klartext-Beschreibungen erzeugen.

| Schritt | Was tun?                                                                                            |
| ------- | --------------------------------------------------------------------------------------------------- |
| 1       | [SKILL.md](https://github.com/LiaScript/LiaSkill/blob/main/SKILL.md) als Datei in den Chat ziehen   |
| 2       | Beschreiben: *„Erstelle einen Kurs zu …, Klassenstufe …, mit … Quizzen und … Differenzierung."*    |
| 3       | Ergebnis im [LiveEditor](https://liascript.github.io/LiveEditor/) prüfen, anpassen                  |

> **Geeignet für:** Lehrkräfte, die heute schon ChatGPT oder Copilot nutzen — kein neues Werkzeug, nur ein angehängtes Dokument.

**************************************

           {{1}}
**************************************

**Stufe 2 — Geführter Prozess in VS Code: der Teaching-Agent**

Die professionelle Variante: [**Teaching-Agent**](https://github.com/LiaScript/teaching-agent) führt Sie in **VS Code mit GitHub Copilot** durch einen vollständigen, strukturierten Kursentwurf — vom Lernziel über die Didaktik bis zum fertigen Material. Statt eines einzelnen Prompts entsteht ein iterativer Dialog mit definierten Phasen:

```ascii
  ┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
  │  FOUNDATION     │ →  │  DIDACTICS      │ →  │  PLANNING       │
  │  Zielgruppe,    │    │  Lehrmethoden,  │    │  Agenda,        │
  │  Lernziele,     │    │  Persona,       │    │  Sitzungs-      │
  │  Umfang         │    │  Stil           │    │  struktur       │
  └─────────────────┘    └─────────────────┘    └─────────────────┘
            │                                              │
            ↓                                              ↓
  ┌─────────────────┐    ┌─────────────────┐
  │  DEVELOPMENT    │ ←  │  FINALIZATION   │
  │  Sitzungen      │    │  Validierung,   │
  │  ausarbeiten    │    │  Export-Bundle  │
  └─────────────────┘    └─────────────────┘
```

> **Geeignet für:** Lehrkräfte, die regelmäßig Material entwickeln und Wert auf didaktische Konsistenz legen — Schul-Curricula, Fortbildungsreihen, fachübergreifende Module.

**************************************

## Teil B: Fünf Wege, einen LiaScript-Kurs zu verbreiten

In [Phase 2](https://liascript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/Cowork_Tutorial_2026/main/02_Verstehen.md) haben wir festgehalten: Ein LiaScript-Kurs ist eine einzelne Markdown-Datei, die im Browser ausgeführt wird. Diese Eigenschaft eröffnet vier sehr unterschiedliche Verbreitungswege — von der niedrigschwelligen URL bis zum vollwertigen SCORM-Paket.

| Weg                 | Was wird geteilt?              | Wofür geeignet?                                          |
| ------------------- | ------------------------------ | -------------------------------------------------------- |
| **Data-URI**        | Ein Link, der den Kurs enthält | Schnelle Vorschau, kurze Materialien, Versand per Mail   |
| **ZIP-Export**      | Alle Dateien als Archiv        | Vollständige Kurse mit Bildern, lokale Nutzung           |
| **Git-Repository**  | Quelle auf GitHub/GitLab       | Kollaborative Entwicklung, Versionierung, dauerhafter Link |
| **SCORM-Paket**     | LMS-fähiges Lernpaket          | Integration in Moodle, OPAL, ILIAS — inkl. Lernstand     |
| **Einbettung von LiaScript in OPAL** |   Ein Link, der den Kurs enthält   | Integration in Moodle, OPAL, ILIAS — inkl. Lernstand     |

### 1. Verbreitung per Data-URI

> [!TIP]
> **Definition** Eine Data-URI ist ein Link, der den vollständigen Kursinhalt direkt in der URL transportiert — keine zusätzliche Datei, kein Server, kein Hosting nötig.

Rufen Sie im LiveEditor das Menü auf und lassen Sie sich eine entsprechende URL generieren. Diese URL können Sie per E-Mail, Chat oder QR-Code weitergeben — beim Öffnen erscheint der vollständige Kurs im LiaScript-Player.

![Teilen per DataURI](Medien/Data_URI.png "Screenshot aus dem LiveEditor. Klicken Sie links oben auf `Menu`")

https://liascript.github.io/course/?data:text/plain;charset=utf-8;Content-Encoding=gzip;base64,H4sIAAAAAAAAAy2Pu26DQBBF+/2KG8dFoojlYdFEcoMiS5bc5EGFsLzAwG4Ca7S7CMsfliqdfyyA3MxDc2bm3ke8CSeQfuwhOiSkbK+oZSzkSDuQG4XFXkvROlwHSFGQRn37a6Y0KgNSmrA7m47auWYMwFocI7ygmOIW5TFaMxbx6Y3W0OdSzhwS1VYL/JDlT9K53r76vhu82pAqyDS8It8qR9avqBZD6/xatVMXBVHsBbGfTMxI5ifk332D1YGk8TDoatZiSznoxhZ3BBUZfKXY3U+vnsHYhoNzvmzMct4HdV3kHG6/drL2qQin+OLF2+A02zW48GWeZWGe/wMaYkYqNAEAAA== 

> [!NOTE]
> **Worauf Sie achten sollten:** Data-URIs werden mit zunehmender Kurslänge sehr lang. Für kurze Materialien (wenige Seiten Text, keine eingebetteten Bilder) ein eleganter Weg — für umfangreichere Kurse stoßen Sie an die URL-Längen­grenzen mancher Mailprogramme und Browser.

### 2. Verbreitung per ZIP-Datei

Im LiaLiveEditor können Sie Ihren Kurs als ZIP-Datei exportieren. Diese Archivdatei enthält alle notwendigen Dateien: die Markdown-Quelle, eingebettete Bilder, lokal referenzierte Ressourcen. Die ZIP-Datei können Sie dann beliebig verbreiten — per Mail, über einen Cloudspeicher, in einem Repositorium.

![alt text](Medien/ZIP_Export.png "Screenshot aus dem LiveEditor. Klicken Sie links oben auf `Menu` und dann auf den kryptischen Zip-Dateinamen")

> [!IMPORTANT]
> **So öffnen die Empfängerinnen und Empfänger das ZIP:** Importieren Sie die ZIP-Datei im Interpreter. Den Import-Dialog öffnen Sie unter https://liascript.github.io/course/.

> [!IMPORTANT]
> **Der entscheidende Vorteil:** Empfängerinnen und Empfänger erhalten die *Quelle* — also den vollen Markdown-Text. Damit greifen alle fünf V-Freiheiten aus [Phase 2](https://liascript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/Cowork_Tutorial_2026/main/02_Verstehen.md) auf: verwahren, verwenden, verarbeiten, vermischen, verbreiten.

Das unmittelbare Laden funktioniert aktuell aus der DropBox heraus. Andere Cloudspeicher (Google Drive, OneDrive) erlauben es nicht, direkt auf die Rohdatei zuzugreifen — hier müssen Sie die ZIP-Datei erst herunterladen und dann im Interpreter importieren.

### 3. Verbreitung über GitHub oder GitLab

Der schmalste Bauplan eines LiaScript-Kurses ist eine einzige Markdown-Datei — und genau das macht Git-Plattformen wie **GitHub** oder **GitLab** zum natürlichen Zuhause für Ihre Materialien. Sie legen den Kurs als Datei in ein Repository, und der LiaScript-Player rendert ihn direkt aus der **Raw-URL** des Repositorys.

> [!TIP]
> **Das Muster:** Hängen Sie die Raw-URL Ihrer Markdown-Datei an den Player-Pfad an:
>
> `https://liascript.github.io/course/?` + Raw-URL
>
> Genau dieses Muster nutzt auch der Badge oben auf jeder Workshop-Phase — schauen Sie sich den Link einmal genauer an.

> [!NOTE]
> **Worauf Sie achten sollten:** Sie brauchen die *Raw-Ansicht* der Datei (auf GitHub den Button „Raw", auf GitLab den Link „Raw" bzw. den `/-/raw/`-Pfad), nicht die hübsch gerenderte Vorschau im Repository.

> [!IMPORTANT]
> **Das ist der OER-Königsweg:** Repository = Quelle + Historie + Lizenz + Zusammenarbeitsplattform in einem. Die fünf V-Freiheiten greifen hier vollständig — und das *kollaborativ*, nicht nur als einseitige Weitergabe.

- **Versionierung:** Jede Änderung ist nachvollziehbar — Sie können jederzeit zu einer früheren Fassung zurückkehren.
- **Kollaboration:** Kolleginnen aus anderen Häusern können per *Pull Request* Verbesserungen vorschlagen, ohne dass Sie ihnen Schreibrechte geben müssen.
- **Dauerhafter Link:** Die URL Ihres Kurses ändert sich nicht — auch wenn Sie Inhalte aktualisieren. Lehrende, die den Link in ihre Moodle-Seite einbinden, müssen nichts nachpflegen.
- **Direkte Importmöglichkeit** Der LiveEditor kann direkt von GitHub oder GitLab importieren — Sie müssen die Datei nicht erst herunterladen.
- **Editor:** Sie können die Dateien in einem komfortableren (Online-)Editor bearbeiten. Drücken Sie auf der Webseite https://github.com/LiaPlayground/Cowork_Tutorial_2026/blob/main/README.md einmal `.`, um die Online-IDE zu öffnen. 

### 4. Export als SCORM-Paket

Mit dem LiaScript Exporter können Sie Ihren Kurs als **SCORM-Paket** exportieren. Dieses Paket lässt sich in jedes LMS hochladen, das SCORM unterstützt — also in Moodle, OPAL, ILIAS und vergleichbare Systeme.

> [!NOTE]
> **Warum das wichtig ist:** SCORM ist der Standard, mit dem Lernmanagementsysteme Inhalte einlesen *und gleichzeitig Lernstand erfassen* — also etwa, ob ein Quiz bearbeitet wurde, welche Antworten gegeben wurden, ob ein Kurs als „abgeschlossen" gilt. Genau diese Anbindung an die LMS-Verwaltung bekommt Ihr LiaScript-Kurs mit dem SCORM-Export — ohne dass der Inhalt seine Markdown-Quelle verliert.

> [!TIP]
> In einem Nextcloud-Ordner der OVGU finden Sie im Ordner bereits ein fertiges SCORM-Paket unseres Selbstlernkurses zum Download. Damit können Sie den Import in Ihrem eigenen Moodle ausprobieren: [https://cloud.ovgu.de/s/GmtpNAXHXztX3NS](https://cloud.ovgu.de/s/GmtpNAXHXztX3NS)

### 5. unmittelbare Einbettung von LiaScript in OPAL

Seid 2025 wird LiaScript neben der SCORM-Integration in OPAL nativ unterstützt. Das heißt: Sie können Ihren Kurs direkt über die Data-URI in OPAL einbetten — ohne den Umweg über den SCORM-Export.

https://bildungsportal.sachsen.de/opal/auth/RepositoryEntry/28960423936?5

> [!IMPORTANT]
> In dieser Situation sind aber keine Lernstandsdaten verfügbar.

## Zusammengefasst

> [!TIP]
> 1. **Data-URI:** Ein Link — ideal für kurze Materialien und schnelle Vorschau.
> 2. **ZIP-Export:** Die vollständige Quelle als Archiv — ideal für OER-Weiternutzung ohne Online-Anbindung.
> 3. **Git-Repository:** Quelle plus Historie plus Lizenz — ideal für gemeinschaftliche Pflege und stabile Links.
> 4. **SCORM-Paket:** Die LMS-Integration — ideal, wenn Anmeldung, Tracking und Notenvergabe gefragt sind.
> 5. **OPAL Embedding:** Direkte Einbettung in OPAL — ideal für schnelle Integration ohne zusätzliche Schritte.
>
> **Die OER-Pointe bleibt erhalten:** In allen fünf Wegen reist der Markdown-Quelltext mit. Wer Ihren Kurs erhält, kann ihn anpassen, weiterentwickeln und in eigenen Kontexten wiederverwenden — genau das macht ihn zur echten Open Educational Resource.