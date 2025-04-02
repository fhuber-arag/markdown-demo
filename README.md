# Dokumentations Tools

[ToC]

# Markdown

Markdown ist ein Format um strukturierte und formatierte Texte zu verfassen. Markdown Dateien (`.md`) sind einfache Textdateien, die mit jedem Texteditor bearbeitet werden können. Ziel des Erfinders der Sprache war es, ein Textformat zu schaffen, das sowohl einfach zu schreiben, als auch einfach zu lesen ist[^mdhistory].

[^mdhistory]: [Wikipedia: Markdown History](https://en.wikipedia.org/wiki/Markdown#History).

## Feature Übersicht

:bulb: Nicht erschrecken, wir gehen in Ruhe auf jedes Feature ein :D

| Feature                     | VS Code            | Joplin                 | [HedgeDoc](https://demo.hedgedoc.org/features) | [GitHub](https://github.com/fhuber-arag/markdown-demo)             | [BitBucket](https://bitbucket.arag.com/users/a503111/repos/markdown-test) |
|----------------------------:|:-------------------|:-----------------------|:--------------------------|:-------------------|:-------------------|
| [Mermaid](#mermaid)         | :white_check_mark: | :white_check_mark:     | :white_check_mark:[^hdmm] | :white_check_mark: | :x:                |
| [PlantUml](#plantuml)       | :white_check_mark: | :package:              | :x:                       | :x:                | :x:                |
| [Graphviz](#graphviz)       | :package:          | :x:                    | :white_check_mark:        | :x:                | :x:                |
| [Abkürzungen](#abkürzungen) | :x:                | :white_check_mark:[^1] | :white_check_mark:        | :x:                | :x:                |
| [Emojis](#emojis)           | :package:          | :white_check_mark:[^1] | :white_check_mark:        | :white_check_mark: | :hankey:           |
| [Fußnoten](#fußnoten)       | :package:[^vsfn]   | :white_check_mark:[^1] | :white_check_mark:        | :white_check_mark: | :x:                |
| [Checkboxen](#checklisten)  | :package:          | :white_check_mark:[^1] | :white_check_mark:        | :white_check_mark: | :x:                |
| [Zitate](#zitate)           | :white_check_mark: | :white_check_mark:     | :white_check_mark::+1:    | :white_check_mark: | :white_check_mark: |

[^hdmm]: Version 9.1.7, ziemlich veraltet. Aktuell ist 11.6
[^vsfn]: Sehen seltsam aus
[^1]: Muss aktiviert werden

## Überschriften

Eine Überschrift wird durch ein oder mehrere Rautezeichen `#` eingeleitet. Die Anzahl der Rauten entspricht dabei der Überschrifen-Ebene, wobei bis zu 6 Ebenen unterstütz werden.

```
# Überschrift 1
## Überschrift 2
### Überschrift 3
#### Überschrift 4
##### Überschrift 5
###### Überschrift 6
```

Viele Tools erstellen aus den Überschriften automatisch Inhaltsverzeichnisse und Navigationsleisten, so dass sich Überschriften hervorragend eignen, ein Markdown Dokument zu strukturieren.

## Textformatierung

Standard Markdown unterstützt die folgenden Formatierungen:

| Schreibweise          | Formatierung        |
|-----------------------|---------------------|
| `*kursiv*`            | *kursiv*            |
| `**fett**`            | **fett**            |
| `***beides***`        | ***beides***        |
| `~~durchgestrichen~~` | ~~durchgestrichen~~ |

Darüber hinaus bieten verschiedene Tools weitergehende Möglichkeiten an:

| Schreibweise                     | Formatierung                   | Unterstützt durch                            |
|----------------------------------|--------------------------------|----------------------------------------------|
| `<font color="red">Farbe</font>` | <font color="red">Farbe</font> | VS Code, Joplin, HedgeDoc, BitBucket         |
| `<ins>unterstrichne</ins>`       | <ins>Unterstrichen</ins>       | VS Code, GitHub, BitBucket, Joplin, HedgeDoc |
| `<marquee>lol</marquee>`         | <marquee>lol</marquee>         | VS Code, Joplin                              |

## Codeblöcke

Ein Codeblock wird durch drei Backticks `` ` `` (Accent Grave) oder drei Tilden `~` eingeleitet:

~~~cpp
class Foo
{

};
~~~

Die Schreibweise mit Tilde kann manchmal notwendig sein, wenn bestimmte externe Programme verwendet werden.

Die meisten Markdown Renderer versuchen die Sprache automatisch zu erkennen; besser ist es jedoch, die Sprache explizit hinter dem dritten Backtick anzugeben (Visual Studio Code bietet innerhalb des Code
Blocks nur Syntax Highlighting an, wenn die Sprache explizit genannt wird).

Eine Liste verfügbarer Sprachen siehe [hier](https://docs.readme.com/rdmd/docs/code-blocks#language-support) oder die [Linguist Dokumentation](https://github.com/github-linguist/linguist/blob/main/lib/linguist/languages.yml).

## Inline Code
Codeschnipsel wie Funktionsnamen, aber auch Dateipfade, können im Fließtext mit einfach Backticks eingefasst werden; das sieht dann so aus: `int main(int, char**)`. **Hinweis**: Einfache Tilde funktioniert leider nicht.

## Listen
Ungeordnete Listen
- Eintrag
- Eintrag
  - Untereintrag
  - Noch einer
- Und so weiter

Nummerierte Listen
1. Test
2. Hallo
3. Welt
3. Die Nummerierung muss nichtmal stimmen :facepalm:

## Tabellen

| Spalte 1    | Spalte 2 | Spalte 3      |
|:------------|:---------:|-------------:|
| Hallo       | Welt      | 42           |
| Foo         | Bar       | 1337         |
| Linksbündig | Zentriert | Rechtsbündig |

## Dateiübergreifende Verknüpfungen
[Beispiel 1](doc/Example.md#beispiel-1)

## Abkürzungen
*[Beispiel]: Mal sehen, ob das funktioniert....nöö :(

Ein Beispiel.

## Zitate

> Dies ist ein zitat
> > Dies ist ein Unterzitat.
> > Für den Fall, dass man mal eine ausgedehnte Email Korrespondenz in Markdown abbilden muss :rofl:

[HedgeDoc](https://demo.hedgedoc.org/features?both#Blockquote-Tags) bietet den Besten Support für Zitate an. Es werden Quellen- und Zeitangaben sowie Farben unterstützt.

## Erweitertes Markdown

### Emojis
Extension: [Markdown Emoji](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-emoji)

:+1: :x: :exploding_head:

### Fußnoten
Extension: [Markdown Footnotes](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-footnotes)

Fußnoten wie diese^[Test] können ebenfalls eingefügt werden.

Es gibt zwei leicht unterschiedliche Syntaxen für Fußnoten. Die erste fügt die Fußnote an Ort und Stelle ein:

```markdown
Dieser Satz hat eine Fußnote^[Und dieser Text wird unten angezeigt]
```

Bei der zweiten Schreibweise sind Verwendung und Definition der Fußnote getrennt (:exclamation: Vorsicht: Das Zirkumflex steht hier **in** dem eckigen Klammerpaar!):

```markdown
Dieser Satz hat ebenfalls eine Fußnote[^ref_footnote_1].

[^ref_footnote_1]: Und dieser Text wird unten angezeigt. Er kann darüber hin aus viel länger sein und mehrmals verwendet werden
```

Beispiel für eine sehr lange Fußnote[^ref_long_footnote].

[^ref_long_footnote]:
    Wer reitet so spät durch Nacht und Wind?

    Es ist der Vater mit seinem Kind;

    Er hat den Knaben wohn in dem Arm,

    Er faβt ihn sicher, er hält ihn warm.

### Checklisten
Extension: [Markdown Checkboxes](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-checkbox)

- [ ] Punkt 1
- [ ] Punkt 2

### Diagramme
Es gibt drei verbreitete Möglichkeiten, Diagramme in Markdown einzubinden:

- [Mermaid](https://mermaid.js.org/)
- [PlantUml](https://plantuml.com/de/)
- [Graphviz](https://graphviz.org/)

Mermaid bietet die breiteste Unterstützung, z.B. durch GitHub.

#### Mermaid

##### Entity Relationship Diagramm
[Dokumentation](https://mermaid.js.org/syntax/entityRelationshipDiagram.html)

```mermaid
---
title: Order example
---
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

##### State Machine
[Dokumentation](https://mermaid.js.org/syntax/stateDiagram.html)

```mermaid
---
title: Simple sample
---
stateDiagram-v2
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

##### Architektur
[Dokumentation](https://mermaid.js.org/syntax/architecture.html)

```mermaid
architecture-beta
    group api(cloud)[API]

    service db(database)[Database] in api
    service disk1(disk)[Storage] in api
    service disk2(disk)[Storage] in api
    service server(server)[Server] in api

    db:L -- R:server
    disk1:T -- B:server
    disk2:T -- B:db
```

##### Mind Map
[Dokumentation](https://mermaid.js.org/syntax/mindmap.html)

```mermaid
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid

```

##### Block Diagramm
[Dokumentation](https://mermaid.js.org/syntax/block.html)

```mermaid
block-beta
columns 1
  db(("DB"))
  blockArrowId6<["&nbsp;&nbsp;&nbsp;"]>(down)
  block:ID
    A
    B["A wide one in the middle"]
    C
  end
  space
  D
  ID --> D
  C --> D
  style B fill:#939,stroke:#333,stroke-width:4px
```

##### Klassendiagramm
[Dokumentation](https://mermaid.js.org/syntax/classDiagram.html)

```mermaid
---
title: Animal example
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
```

##### Git Graph
[Dokumentation](https://mermaid.js.org/syntax/gitgraph.html)

```mermaid
---
title: Example Git diagram
---
gitGraph
   commit
   commit
   branch develop
   checkout develop
   commit
   commit
   checkout main
   merge develop
   commit
   commit
```

##### Gantt
[Dokumentation](https://mermaid.js.org/syntax/gantt.html)

```mermaid
gantt
    title A Gantt Diagram
    dateFormat YYYY-MM-DD
    section Section
        A task          :a1, 2014-01-01, 30d
        Another task    :after a1, 20d
    section Another
        Task in Another :2014-01-12, 12d
        another task    :24d
```

##### User Journey
[Dokumentation](https://mermaid.js.org/syntax/userJourney.html)

```mermaid
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 5: Me
```

##### Flow Chart
[Dokumentation](https://mermaid.js.org/syntax/flowchart.html)

```mermaid
flowchart TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]
```

##### Tortendiagramm
[Dokumentation](https://mermaid.js.org/syntax/pie.html)

```mermaid
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
```

##### C4 Diagramm

[Dokumentation](https://mermaid.js.org/syntax/c4.html)

[C4 Website](https://c4model.com/)

```mermaid
    C4Context
      title System Context diagram for Internet Banking System
      Enterprise_Boundary(b0, "BankBoundary0") {
        Person(customerA, "Banking Customer A", "A customer of the bank, with personal bank accounts.")
        Person(customerB, "Banking Customer B")
        Person_Ext(customerC, "Banking Customer C", "desc")

        Person(customerD, "Banking Customer D", "A customer of the bank, <br/> with personal bank accounts.")

        System(SystemAA, "Internet Banking System", "Allows customers to view information about their bank accounts, and make payments.")

        Enterprise_Boundary(b1, "BankBoundary") {

          SystemDb_Ext(SystemE, "Mainframe Banking System", "Stores all of the core banking information about customers, accounts, transactions, etc.")

          System_Boundary(b2, "BankBoundary2") {
            System(SystemA, "Banking System A")
            System(SystemB, "Banking System B", "A system of the bank, with personal bank accounts. next line.")
          }

          System_Ext(SystemC, "E-mail system", "The internal Microsoft Exchange e-mail system.")
          SystemDb(SystemD, "Banking System D Database", "A system of the bank, with personal bank accounts.")

          Boundary(b3, "BankBoundary3", "boundary") {
            SystemQueue(SystemF, "Banking System F Queue", "A system of the bank.")
            SystemQueue_Ext(SystemG, "Banking System G Queue", "A system of the bank, with personal bank accounts.")
          }
        }
      }

      BiRel(customerA, SystemAA, "Uses")
      BiRel(SystemAA, SystemE, "Uses")
      Rel(SystemAA, SystemC, "Sends e-mails", "SMTP")
      Rel(SystemC, customerA, "Sends e-mails to")

      UpdateElementStyle(customerA, $fontColor="red", $bgColor="grey", $borderColor="red")
      UpdateRelStyle(customerA, SystemAA, $textColor="blue", $lineColor="blue", $offsetX="5")
      UpdateRelStyle(SystemAA, SystemE, $textColor="blue", $lineColor="blue", $offsetY="-10")
      UpdateRelStyle(SystemAA, SystemC, $textColor="blue", $lineColor="blue", $offsetY="-40", $offsetX="-50")
      UpdateRelStyle(SystemC, customerA, $textColor="red", $lineColor="red", $offsetX="-50", $offsetY="20")

      UpdateLayoutConfig($c4ShapeInRow="3", $c4BoundaryInRow="1")
```

#### PlantUml
Extension: [Markdown Plantuml Preview](https://marketplace.visualstudio.com/items?itemName=myml.vscode-markdown-plantuml-preview)

[:link: PlantUml Website](https://plantuml.com/de/)

##### Sequenz Diagramm

```plantuml
@startuml

start

if (Graphviz installed?) then (yes)
  :process all\ndiagrams;
else (no)
  :process only
  __sequence__ and __activity__ diagrams;
endif

stop

@enduml
```

##### Klassendiagramm
```plantuml
@startuml
skinparam classAttributeIconSize 0
class Dummy {
 -field1
 #field2
 ~method1()
 +method2()
}

@enduml
```

##### Bewertung
- Veraltete Optik, etwas klobig und relativ schlechte Tool-Unterstützung
- Beste Klassendiagramme (Subjektiv?)

#### Graphviz
```graphviz
digraph finite_state_machine {
    rankdir=LR;
    size="8,5"

    node [shape = doublecircle]; S;
    node [shape = point ]; qi

    node [shape = circle];
    qi -> S;
    S  -> q1 [ label = "a" ];
    S  -> S  [ label = "a" ];
    q1 -> S  [ label = "a" ];
    q1 -> q2 [ label = "ddb" ];
    q2 -> q1 [ label = "b" ];
    q2 -> q2 [ label = "b" ];
}
```

# Bedeutung der Datei README.md

Ist in einem GitHub oder Bitbucket Repository eine Datei `README.md` vorhanden, wird sie im Browser unterhalb der Quelldateien Verzeichnisses gerendert.

Eine gute `README.md` sollte beinhalten:

- Kurze Beschreibung des Projekts in ein, zwei Sätzen
- Schritte zum selber Bauen (inklusive Abhängigkeiten)
- Wie wird die Entwicklungsumgebung eingerichtet?
- Wie kann ich beitragen?
- Kontakt zu anderen Entwicklern (Foren, Discord, etc)

Oft auch enthalten sind:

- Code of Conduct
- CI/CD Status
- Achkowledgements / Hall of Fame
- Lizenzinformationen

## Beispiele

- [RTTR](https://github.com/rttrorg/rttr)
- [Roslyn](https://github.com/dotnet/roslyn)
- [EF Core](https://github.com/dotnet/efcore)
- [Git Diagram](https://github.com/ahmedkhaleel2004/gitdiagram?tab=readme-ov-file) (Viele Emojis ;))

# Tools

## Visual Studio Code

### Out of the Box
Visual Studio Code bietet Out of the Box eine gute Unterstützung für Markdown, sowohl Syntaxhighlighting für `.md` Dateien, als auch Rendering für eine Vorschau.

### Vorschau anzeigen
Um die Markdown Vorschau anzuzeigen, kann die Tastenkombination

    [Ctrl]-[K], V

verwendet werden, oder über die Kommando-Palette (`[Strg]-[Shift]-[P]`)

    > Markdown: Open Preview

### Erweiterungen

Empfohlene Plugins für Markdown:

- [Markdown Preview Mermaid Support](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid)
- [Markdown Checkboxes](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-checkbox)
- [Markdown Emoji](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-emoji)
- [Markdown Footnotes](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-footnotes)
- [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles) (Optional)

Funktionieren eher schlecht als recht:

- [Markdown Plantuml Preview](https://marketplace.visualstudio.com/items?itemName=myml.vscode-markdown-plantuml-preview)
- [Graphviz Markdown Preview](https://marketplace.visualstudio.com/items?itemName=geeklearningio.graphviz-markdown-preview)
- [Markdown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf)

## Joplin

[:link: Joplin Markdown Guide](https://joplinapp.org/help/apps/markdown/)

Joplin ist eine Desktop- und Mobile App, mit der sich Notizen in Markdown verfassen und verwalten lassen. Es ist möglich, persönliche Notizen über Cloudspeicher wie OneDrive, Google Drive und DropBox zu Synchronisieren und zwischen mehreren Geräten zu teilen.

Das Teilen von Notizbüchern mit anderen Leuten ist schwierig, wenn nicht die kostenpflichtige Joplin Cloud verwendet wird (Preise ähnlich hoch wie Confluence).

## HedgeDoc :hedgehog:

[:link: HedgeDoc](https://hedgedoc.org/) ist ein Server für kollaborative Dokumentation mit Markdown. Es ist ein OpenSource Projekt und muss (kann! :heart_eyes:) aktuell selbst gehostet werden.

## GitHub

[:link: Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github)

[:link: GitHub Flavored Markdown Spec](https://github.github.com/gfm/)

## BitBucket

[:link: BitBucket Markdown Tutorial](https://bitbucket.org/tutorials/markdowndemo/src/master/)

## Structurizr
[:link: Hennings Structurizr Server](https://c4.nitschke.dyndns.org/dashboard?continue)

## Pandoc

[Pandoc](https://pandoc.org/) ist ein Konsolenbasiertes Werkzeug, mit dem eine große Zahl von Textformaten ineinander konvertiert werden können, unter anderem Markdown.

Die Konvertierung kann wie folgt angestoßen werden:

```bash
pandoc README.md -o README.pdf
```

Die Option `-o` spezifiziert die zu erstellende Datei; das Ausgabeformat wird anhand der Dateiendung erkannt, kann aber auch mit der Option `-t` explizit angegeben werden (s.u.).

Interessante Ausgabeformate sind u.a.:
- `docx`(Word)
- `pdf` (PDF)
- `html` (HTML5)
- `latex` (LaTeX)
- `epub` (EPUB v3)
- `opendocument` (OpenOffice Dokument)
- `pptx` (PowerPoint)

Für eine vollständige Liste der Formate, s. `-t FORMAT` in [Pandoc Options](https://pandoc.org/MANUAL.html#options).

# Architektur-Dokumentation

## UML

UML ist eine sehr formale Sprache, mit der ein System bis ins kleinste Detail spezifiziert werden kann^[Bis hin zur Variante SysML, mit der auch physische Interaktionen im Nanosekunden und Mikrogrammbereich spezifiziert werden]. Die Diagramme, die dabei herauskommen, sind in den allermeisten Fällen überfrachtet und fast unbenutzbar - dazu ein Negativbeispiel:

![Negativbeispiel](https://www.uml-diagrams.org/examples/class-example-dicom-app-hosting-api.png)

Dies ist sinnvoll beim Klassischen Wasserfall- oder Spiralmodell und bei Projekten, bei denen viele Akteure im Vorfeld genauestens abstimmen müssen, was genau geliefert werden muss (Stichwort: Lastenheft). Für agile Projekte bieten sich andere Ansätze an, die mehr "light weight" sind.

## C4

[:link::movie_camera: Einführendes Video des Erfinders (🇬🇧 Englisch)](https://www.youtube.com/watch?v=x2-rSnhpw0g)

Das C4 Modell organisiert die Sicht auf eine Softwarearchitektur auf vier Ebenen, die von einer High-Level Übersicht (Ebene 1) bis hin zur Code-Ebene (Ebene 4) sukkzessive in die Architektur "hinein zoomen".


| Ebene | Sichtweise | Erklärung                                                | Analogie |
|------:|------------|----------------------------------------------------------|------------------------------|
| 1     | Context    | Grobe Sicht auf das System. Mit welchen anderen System arbeiten wir zusammen (Datenbanken, REST Dienstem ...)? | :earth_africa: Weltkarte |
| 2     | Containers | Zeigt die Bestandteile eines Systems (In C4 "Container" genannt). Beispiele sind Desktop Applikationen, SPAs, REST Dienste, etc. | :city_sunrise: Stadt
| 3     | Components | Zeigt Komponenten eines einzelnen Containers. Dies sind **High-Level** Abstraktionen, auf keinen Fall Klassen und Funktionen! Beispiele: "Login Controller", "Todo Item Data Source". | :house_with_garden: Stadtteil |
| 4     | Code       | Detailierteste Ebene, einzelne Klassen, Funktionen etc. | :microscope: Straße |

:exclamation: Der Erfinder von C4 rät ausdrücklich davon ab, sich auf Ebene 4 zu bewegen, außer es ist unbedingt erforderlich.

- [Mermaid](https://mermaid.js.org/syntax/c4.html) bietet gute Unterstützung für (statische) C4 Diagramme
- [Structurizr](https://structurizr.com) ist eine interaktive Lösung, bei der Diagramme auch verknüpft werden können. Das ermöglicht die Navigation in der Architektur. Außerdem werden Animationen angeboten, mit denen sich bestimmte Sachverhalte Stück für Stück erklären lassen

### Mermaid

Context Diagramm

```mermaid
 C4Context
  title Neuer VSK Client (Components)
  
  %% Personen
  Person(vskUser, "Benutzer", "Benutzer des VSK Systems, z.B. Sachbearbeiter")

  %% Systeme
  System(sysWebApp, "Angular Web Application", "")
  System(sysProxy, "Proxy", "Proxy Dienst. Dollmetscher zwischen Backend und WebApp")
  System(sysBackend, "vgstmain", "Vorgangssteuerung. Alles wie bisher")
  System(sysDatabase, "DB", "Die gute alte Datenbank")

  %% Beziehungen zwischen Benutzern und Systemen
  BiRel(vskUser, sysWebApp, "")  
  BiRel(sysWebApp, sysProxy, "")
  BiRel(sysProxy, sysBackend, "")
  BiRel(sysBackend, sysDatabase, "")

  UpdateLayoutConfig($c4ShapeInRow="2", $c4BoundaryInRow="1")
```

Container Diagramm

```mermaid
C4Container
  title Container Diagramm für Angular Web Application
  
  %% Externes System
  System_Ext(sysProxy, "Proxy", "Java")
  
  %% Person
  Person(user, "Sachbearbeiter")
  
  %%ContainerDb_Ext(database, "DB2") 

  Container_Boundary(contAngular, "Angular Web Application") {
    Container(contVskComponents, "VSK Components", "TypeScript", "Wiederverwendbare Steuerelemente")
    Container(web_app, "Web Application", "Java, Spring MVC", "Delivers the static content and the Internet banking SPA")  
  }

  Rel(user, web_app, "Aufruf im Browser")
  Rel(web_app, contVskComponents, "Verwendet")
  Rel(web_app, sysProxy, "Datenaustausch im JSON Format")
```

### Structurizr

# Code Dokumentation

## Doxygen

[Doxygen Website](https://www.doxygen.nl/)

## Javadoc
[How to Write Doc Comments for the Javadoc Tool (Oracle)](https://www.oracle.com/de/technical-resources/articles/java/javadoc-tool.html)

## JSDoc

[JSDoc Reference](https://www.typescriptlang.org/docs/handbook/jsdoc-supported-types.html)