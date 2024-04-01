---
handout: false
title: Demo - Charts with Mermaid
author: hasp
date: 2024-03-20
header: ${author} - ${title} - ${date}
footer: ${pageNo}/${pageCount}

theme: beige
revealOptions:
  transition: "fade"
---

# Charts with Mermaid

```mermaid
graph LR
  A[From A] --> B --> C[...] --> Y --> Z[to Z]
```

---

## Optional Styling

### Use YAML frontmatter within `mermaid`-code block

> See [Directives](https://mermaid.js.org/config/directives.html) and [Mermaid Theme Config](https://mermaid.js.org/config/theming.html)

---

## Examples

- set a title with `title`
- `config`:
  - `theme`: _[base, default, forest, dark, neutral, null]_
    - use `base` when you want your own coloring (see below)
  - `themeVariables`:
    - `fontFamily`: _[sans-serif, serif, monospace]_ or use local installed fonts
    - Colors - CSS name, rgb(hex - preferred), or hsv:
    - `textColor`, `lineColor`,
    - `primaryColor`, `primaryTextColor`, `primaryBorderColor`,
    - same for `secondaryColor`, `tertiaryColor`

---

## Pie Chart - Mermaid Graph

```mermaid
---
title: Unicorn Colors
startOnLoad: true
config:
  theme: base
  themeVariables:
    textColor: purple
    primaryColor: aqua
    secondaryColor: pink
    tertiaryColor: violet
    fontFamily: sans-serif
---
pie
    "Unicorns" : 190
    "Cats" : 320
    "Rats" : 150
    "Dogs": 100
    "Chicken": 30
```

---

## Pie Chart - Mermaid Code

```yaml
---
title: Unicorn Colors
config:
  theme: base
  themeVariables:
    textColor: purple
    primaryColor: aqua
    secondaryColor: pink
    tertiaryColor: violet
    fontFamily: sans-serif
---
pie
    "Unicorns" : 190
    "Cats" : 320
    "Rats" : 150
    "Dogs": 100
    "Chicken": 30
```

---

## Graph

##### with coloring!

```mermaid
---
title: your graph title
config:
  theme: base
  themeVariables:
    textColor: purple
    lineColor: purple
    primaryColor: aqua
    primaryTextColor: purple
    primaryBorderColor: purple
    secondaryColor: pink
    tertiaryColor: violet
    fontFamily: sans-serif
---
graph LR;
    A--> B & C & D;
    B--> A & E;
    C--> A & E;
    D--> A & E;
    E--> B & C & D;
```

---

## Flowchart

```mermaid
---
title: Go with the Flow
startOnLoad: true
securityLevel: loose
config:
  theme: base
  themeVariables:
    primaryColor: aqua
    secondaryColor: pink
    tertiaryColor: violet
    fontFamily: sans-serif
font-info: [sans-serif, serif, monospace, ...]
theme-info: [base, default, forest, dark, neutral, null]
---
flowchart LR
  A[Hello and some more text] --> B[World]
```

---

## Timeline

```mermaid
---
title: History of Social Media Platform
config:
  theme: neutral
  themeVariables:
    fontFamily: sans-serif
font-info: [sans-serif, serif, monospace, ...]
theme-info: [base, default, forest, dark, neutral, null]
---
timeline
    title History of Social Media Platform
    section early bird
      2002 : LinkedIn
    section late bloomer
      2004 : Facebook
           : Google
      2005 : Youtube
      2006 : Twitter
    section the unknown
      20xx : discord
```

---

## XY-Chart

##### still with sizing problems

```mermaid
---
config:
  theme: forest
  themeVariables:
    fontFamily: serif
---
xychart-beta
    title "Sales Revenue"
    x-axis [jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec]
    y-axis "Revenue (in $)" 4000 --> 11000
    bar [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
    line [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
```

---

## State Diagram

### with coloring

```mermaid
stateDiagram
   direction TB

   accTitle: This is the accessible title
   accDescr: This is an accessible description

   classDef notMoving fill:white
   classDef movement font-style:italic
   classDef badBadEvent fill:#f00,color:white,font-weight:bold,stroke-width:2px

   [*]--> Still
   Still --> [*]
   Still --> Moving
   Moving --> Still
   Moving --> Crash
   Crash --> [*]

   class Still notMoving
   class Moving, Crash movement
   class Crash badBadEvent
   class end badBadEvent
```
