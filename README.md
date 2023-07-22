
### Docusaurus 3 + Quarto regression example

Docusaurus 3 alpha has been released https://github.com/facebook/docusaurus/discussions/9073

Rendering MDX inside .qmd files breaks, being rendered as plain text not as components.

<img width="1036" alt="examples" src="https://github.com/quarto-dev/quarto-cli/assets/54409/a64db34b-3652-44f8-8d3c-a207379b5a8d">

### Steps to reproduce

Install the package.json with yarn and you should see the problems when rendering Docusaurus with quarto preview or inside VSCode. Here's Docusaurus 3 install documentation in case of any issues: https://docusaurus.io/community/canary

Here's the broken citations repo on Docusaurus 2.4: https://github.com/krishaamer/quarto-broken-citations-reproducible

And in this the branch the broken Docusaurus 3 alpha integration. I also tested the canary from 21/07/2023 and it's the same as the alpha.
https://github.com/krishaamer/quarto-broken-citations-reproducible/tree/docusaurus-3

### Expected behavior

Imports, code and citations should be transformed and rendered.

### Actual behavior

Nothing is transformed or rendered. Imports, code, and citations are displayed as play text.

### Your environment

```
MacOS Ventura 13.4 (22F66)

Visual Studio Code Version: 1.80.1
Commit: 74f6148eb9ea00507ec113ec51c489d6ffb4b771
Date: 2023-07-12T17:20:23.298Z
Electron: 22.3.14
ElectronBuildId: 21893604
Chromium: 108.0.5359.215
Node.js: 16.17.1
V8: 10.8.168.25-electron.0
OS: Darwin x64 22.5.0

VSCode Quarto extension v1.90.0
Zotero 6.0.26
Docusaurus 3.0.0-alpha.0 (2023-06-15)
```

### Quarto check output

```
quarto check

[✓] Checking versions of quarto binary dependencies...
      Pandoc version 3.1.6: OK
      Dart Sass version 1.55.0: OK
      Deno version 1.33.4: OK
[✓] Checking versions of quarto dependencies......OK
[✓] Checking Quarto installation......OK
      Version: 1.4.251
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
