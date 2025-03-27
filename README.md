# Out of the Box
Visual Studio Code bietet Out of the Box eine gute Unterstützung für Markdown, sowohl Syntaxhighlighting für `.md` Dateien, als auch Rendering für eine Vorschau.

## Vorschau anzeigen
Um die Markdown Vorschau anzuzeigen, kann die Tastenkombination

    [Ctrl]-[K], V

verwendet werden, oder über die Kommando-Palette:

    > Markdown: Open Preview

## Codeblöcke

```cpp
class Foo
{

};
```

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

# Erweiterungen

## Diagramme

### Mermaid
Extension: [Markdown Preview Mermaid Support](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid)

#### Entity Relationship Diagramm

```mermaid
---
title: Order example
---
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

### PlantUml
Extension: [Markdown Plantuml Preview](https://marketplace.visualstudio.com/items?itemName=myml.vscode-markdown-plantuml-preview)

[:link: PlantUml Website](https://plantuml.com/de/)

#### Sequenz Diagramm

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

#### Test
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

### Graphviz
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

## Emojis
Extension: [Markdown Emoji](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-emoji)

:+1: :x: :exploding_head:

## Fußnoten
Extension: [Markdown Footnotes](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-footnotes)

Fußnoten wie diese^[Test] können ebenfalls eingefügt werden.

## Checklisten
Extension: [Markdown Checkboxes](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-checkbox)

- [ ] Punkt 1
- [ ] Punkt 2

