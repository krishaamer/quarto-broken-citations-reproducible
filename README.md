# quarto-broken-citations-reproducible

### Bug description

Hi, I'm using Quarto + VSCode + Docusaurus to write a thesis and after upgrading to latest version citations stopped working in Docusaurus. The [@somequotation] are not rendering anymore but just remain unchanged in the output. Rendering to PDF still works fine. Please advise.

### Steps to reproduce

`abstract.qmd:`
```
---
title: Abstract
bibliography: [ref.bib]
csl: apa.csl
sidebar_position: 1
editor:
    render-on-save: false
---

Example quote: [@circleeconomyCircularityGapReport2022] says blablaba.
```

### Expected behavior

Citation [@circleeconomyCircularityGapReport2022] should be transformed into a reference.

### Actual behavior

[@circleeconomyCircularityGapReport2022] remains untransformed.

### Your environment

- MacOS Ventura 13.4 (22F66)
- Visual Studio Code Version: 1.79.2
Commit: 695af097c7bd098fbf017ce3ac85e09bbc5dda06
Date: 2023-06-14T08:58:52.392Z
Electron: 22.5.7
Chromium: 108.0.5359.215
Node.js: 16.17.1
V8: 10.8.168.25-electron.0
OS: Darwin x64 22.5.0
- VSCode Quarto extension v1.88.0
- Zotero 6.0.26
- Docusaurus 2.4.0

### Quarto check output

```
[✓] Checking versions of quarto binary dependencies...
      Pandoc version 3.1.2: OK
      Dart Sass version 1.55.0: OK
      Deno version 1.33.2: OK
[✓] Checking versions of quarto dependencies......OK
[✓] Checking Quarto installation......OK
      Version: 1.4.176
      Path: /Applications/quarto/bin

[✓] Checking basic markdown render....OK

[✓] Checking Python 3 installation....OK
      Version: 3.10.9 (Conda)
      Path: /Users/krishaamer/anaconda3/bin/python
      Jupyter: 5.2.0
      Kernels: python3

[✓] Checking Jupyter engine render....OK

[✓] Checking R installation...........OK
      Version: 4.3.1
      Path: /Library/Frameworks/R.framework/Resources
      LibPaths:
        - /Library/Frameworks/R.framework/Versions/4.3-x86_64/Resources/library
      knitr: 1.43
      rmarkdown: 2.22

[✓] Checking Knitr engine render......OK

```

### Quarto preview output

```
quarto preview /Users/krishaamer/Desktop/current/green-filter-research/research/abstract.qmd --no-browser --no-watch-inputs
(base) krishaamer@Kriss-MacBook-Pro-2 green-filter-research % quarto preview /Users/krishaamer/Desktop/current/green-filter-research/research/abstract.qmd --no-browser --no-watch-inputs
pandoc 
  to: >-
    markdown_strict+raw_html+all_symbols_escapable+backtick_code_blocks+fenced_code_blocks+space_in_atx_header+intraword_underscores+lists_without_preceding_blankline+shortcut_reference_links+autolink_bare_uris+emoji+footnotes+gfm_auto_identifiers+pipe_tables+strikeout+task_lists+tex_math_dollars+pipe_tables+tex_math_dollars+header_attributes+raw_html+all_symbols_escapable+backtick_code_blocks+fenced_code_blocks+space_in_atx_header+intraword_underscores+lists_without_preceding_blankline+shortcut_reference_links
  output-file: abstract.md
  standalone: true
  default-image-extension: png
  wrap: none
  html-math-method: webtex
  
metadata
  title: Abstract
  bibliography:
    - ref.bib
  csl: apa.csl
  sidebar_position: 1
  editor:
    render-on-save: false
  
Output created: abstract.md

Preparing to preview

Watching files for changes
Preview service running (7224)

> docusaurus
> docusaurus start --no-open --port 4027 --host 127.0.0.1

[INFO] Starting the development server...
[SUCCESS] Docusaurus website is running at: http://127.0.0.1:4027/
ℹ Compiling Client
✔ Client: Compiled successfully in 2.67s
Browse at http://localhost:4027/
client (webpack 5.87.0) compiled successfully
ℹ Compiling Client
✔ Client: Compiled successfully in 403.70ms
client (webpack 5.87.0) compiled successfully
ℹ Compiling Client
✔ Client: Compiled successfully in 242.15ms
client (webpack 5.87.0) compiled successfully

```
