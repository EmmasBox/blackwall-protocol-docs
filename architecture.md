---
layout: default
title: Architecture
has_toc: false
---

# Architecture of Blackwall

Below you can see a simplified architecture flowchart

<pre class="mermaid">
flowchart TD
    style BLACKWALL fill:#a11616,color:#fff,stroke:#2b2a33
    BLACKWALL(["Blackwall program"])
    PYTHON(["Python"])
    TEXTUAL(["Textual application"])
    BLACKWALL --> TEXTUAL
    BLACKWALL --- PYTHON
    TEXTUAL --> COMMANDLINE
    PYTHON --- TEXTUAL

    style TABS fill:#a11616,color:#fff,stroke:#2b2a33
    TABS(["Tab system"])
    TEXTUAL --> TABS
    TABS --> PANELS

    style BLACKWALLSCREENS fill:#a11616,color:#fff,stroke:#2b2a33
    BLACKWALLSCREENS(["Blackwall screens"])
    TEXTUAL --> BLACKWALLSCREENS

    style COMMANDLINE fill:#a11616,color:#fff,stroke:#2b2a33
    COMMANDLINE(["Blackwall command line"])
    SUBPROCESS(["Python subprocess"])
    TSOCMD(["TSOCMD"])
    ZOSCOMMAND(["Command executed on z/OS"])
    
    COMMANDLINE --> SUBPROCESS
    SUBPROCESS --> TSOCMD
    TSOCMD --> ZOSCOMMAND

    ZOAU(["Z Open Automation Utilities (optional)"])
    ZOS(["z/OS"])
    ZOS --> ZOAU
    ZOAU --> TEXTUAL

    style PANELS fill:#a11616,color:#fff,stroke:#2b2a33
    PANELS(["Blackwall tab panels"])
    style WRAPPER fill:#a11616,color:#fff,stroke:#2b2a33
    WRAPPER(["Blackwall API wrapper"])
    RACFU(["RACFU"])
    COREAPI(["IRRSEQ00 and IRRSMO00"])
    SAF(["SAF"])
    RACF(["RACF"])
    PANELS <--> WRAPPER
    WRAPPER <--> RACFU
    RACFU <--> COREAPI
    COREAPI <--> SAF
    SAF <--> RACF
</pre>
