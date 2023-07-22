---
title: Broken Examples
bibliography: [ref.bib]
csl: chicago.csl
sidebar_position: 3
editor:
    render-on-save: false 
---

## MDX {#mdx}

**MDX remains untransformed and is shown as plain text**

``` text
import Image from "@theme/IdealImage";
import Runaround from './runaround.png'
```

```mdx-code-block
import Image from "@theme/IdealImage";
import Runaround from './runaround.png'
```


```mdx-code-block
<Image img={Runaround} alt="Runaround" />
```

## Citations {#citations}

**Citations remain unrendered even though they exist in the ref.bib**

Could a machine imitate a human being so well that one would be
deceived, without realizing one is talking to an AI?
@turingCOMPUTINGMACHINERYINTELLIGENCE1950.

