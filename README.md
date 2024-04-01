---
title: reveal-md slides
author: hasp
---

# tmpl-reveal-md

Template / Introductory Repository to explain markdown slide creation with reveal-md.

> [!Warning]
> ⚠️**Work in Progress!**

---

## Installation / Update

1. install node.js: `winget install OpenJS.NodeJS.LTS`
2. install reveal-md: `npm install -g reveal-md`
3. update/upgrade all global packages:
   - `npm update -g`
   - `npm upgrade -g`

---

## Usage

- To show **all documents** of `lectures` and `exercise` folder:
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

---

### TODOs

- consider to update `mermaid.min.js` every now and then
  - atm version 10.9.0 is used
  - see/download [mermaid.min.js](https://cdnjs.cloudflare.com/ajax/libs/mermaid/10.9.0/mermaid.min.js) from CDN
- Improvement of `README.md` ... 😜
- Add `reveal-md.json` and `.reveal`-folder to other templates

---

## Mermaid Problems

> [!WARNING]
> ⚠️ Mermaid not working as intended<br> (see this [issue](https://github.com/webpro/reveal-md/issues/197))

1. **Settings Error**: settings not working in:
   - `reveal-md.json` and
   - YAML Frontmatter of `.md`-files
2. **Display Error**: the mermaid graph size is often not correctly show

> Another problem (of reveal-md):<br> `favicon.ico` not working as intended

---

## Mermaid Workarounds

1. **Settings Error**: add mermaid settings directly to diagram (as frontmatter)
2. **Display error**: refresh the browser (`Ctrl+R`) for redraw
   - this needs the setting `"history": true` in `reveal-md.json`
   - otherwise you start at slide one.- use Typora and vscode!
