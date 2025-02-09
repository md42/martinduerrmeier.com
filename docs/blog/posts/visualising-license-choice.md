---
date:
  created: 2025-02-09
tags:
  - TIL
---
# Which license to choose for a git repo?

TIL [Codeberg](https://codeberg.org)[^1] has a [help text](https://docs.codeberg.org/getting-started/licensing/) to choose a license when creating a git repository.  
That is handy! Let's make a [Mermaid Flowchart](https://mermaid.js.org/syntax/flowchart.html) for that. I find that better to read then the pure text.

``` mermaid
flowchart TD
    A[Do you either want to allow people to create proprietary closed-source projects with your code, or do you expect your project to remain small e.g. less than 300 lines?]
    
    A -- "No" --> B[Do you want to allow people to create a closed-source service, for example by using your code on a web server without releasing the source code?]
    A -- "Yes" --> D[Do you want to be able to sue users of your code for patent infringement implemented in the code?]
    
    B -- "No" --> AGPL[We recommend using the **AGPL-3.0-or-later** license]
    B -- "Yes" --> C[Do you want to allow people to use your code as a library and not disclose the source-code of their main program?]
    
    C -- "No" --> GPL[We recommend using the **GPL-3.0-or-later** license]
    C -- "Yes" --> LGPL[We recommend using the **LGPL-3.0-or-later** license]
    
    D -- "No" --> Apache[We recommend using the **Apache-2.0** license]
    D -- "Yes" --> MIT[We recommend using the **MIT** license]
```

[^1]: Codeberg is a non-profit, community-led effort that provides Git hosting and other services for free and open source projects. It is a privacy-friendly alternative to commercial services such as GitHub.
