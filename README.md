---
title: README
author: hasp
---

# Introduction to MS 365 Admin Center

## Start with
## ➡️ [INTRO](./00-Intro-MS365-Admin-Center.md) ⬅️

---

<!-- .slide: data-background-image="https://media.tenor.com/AVa6-PqQpuMAAAAC/emergency-stop-button-emergency.gif" data-background-opacity="0.2" -->

## ⛔ STOP!

>  Ignore the following text! This is just needed if you are interested in `reveal-md`!

---

## Info - `reveal-md`

Template / Introductory Repository to explain markdown slide creation with reveal-md.

---

## Installation / Update

1. install node.js: `winget install OpenJS.NodeJS.LTS`
2. install reveal-md: `npm install -g reveal-md`
3. update/upgrade all global packages:
   - `npm update -g`
   - `npm upgrade -g`

---

## Usage

- To show **all documents**:
  - stay in root-folder of repository
  - and start: `reveal-md . -w`
    - `-w` is optional and watches for file changes
- To show **a specific document** (using this readme as example):
  - `reveal-md README.md`
- For parameter overview just type `reveal-md`
- Slide creation: use [Typora](https://typora.io/) and [vscode](https://code.visualstudio.com/).
- See the various slides to get an idea whats possible

---

## Important files

- global configuration: `reveal-md.json`
- can be overwritten by YAML frontmatter in `md`-files
- folder `.reveal`:
  - css styling (`style.css`)
  - mermaid plugin (`mermaid.min.js`)

---

## Important Links

- Our slides tool: <https://github.com/webpro/reveal-md>
- Based on this HTML slide tool: <https://revealjs.com/>
- Code highlighting: <https://highlightjs.org/demo>
- Mermaid graphs: <https://mermaid.js.org/>
  - especially the [docs](https://mermaid.js.org/intro/)
  - consider the mermaid [live editor](https://mermaid.live)
