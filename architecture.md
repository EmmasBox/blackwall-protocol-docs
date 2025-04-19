---
layout: default
title: Architecture
has_toc: false
---

# Architecture of Blackwall

Below you can see a simplified architecture flowchart.

**RED** indicates that it is a part of Blackwall

**GREEN** indicates it is tied to Python

**YELLOW** indicates it is part of z/OS or a core subsystem

**BLUE** indicates it is a third party Python package

<pre class="mermaid">
flowchart TD
    style BLACKWALL fill:#a11616,color:#fff,stroke:#2b2a33
    BLACKWALL(["Blackwall program"])
    style PYTHON fill:#44D22E,color:#fff,stroke:#2b2a33
    PYTHON(["Python"])
    style TEXTUAL fill:#2EC1D2,color:#fff,stroke:#2b2a33
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
    style SUBPROCESS fill:#44D22E,color:#fff,stroke:#2b2a33
    SUBPROCESS(["Python subprocess"])
    style TSOCMD fill:#FFC508,color:#fff,stroke:#2b2a33
    TSOCMD(["TSOCMD"])
    style ZOSCOMMAND fill:#FFC508,color:#fff,stroke:#2b2a33
    ZOSCOMMAND(["Command executed on z/OS"])
    COMMANDLINE --> SUBPROCESS
    SUBPROCESS --> TSOCMD
    TSOCMD --> ZOSCOMMAND
    
    style ZOAU fill:#2EC1D2,color:#fff,stroke:#2b2a33
    ZOAU(["Z Open Automation Utilities (optional)"])
    style ZOS fill:#FFC508,color:#fff,stroke:#2b2a33
    ZOS(["z/OS"])
    ZOS --> ZOAU
    ZOAU --> TEXTUAL

    style PANELS fill:#a11616,color:#fff,stroke:#2b2a33
    PANELS(["Blackwall tab panels"])
    style WRAPPER fill:#a11616,color:#fff,stroke:#2b2a33
    WRAPPER(["Blackwall API wrapper"])
    style RACFU fill:#2EC1D2,color:#fff,stroke:#2b2a33
    RACFU(["RACFU"])
    style COREAPI fill:#FFC508,color:#fff,stroke:#2b2a33
    COREAPI(["IRRSEQ00 and IRRSMO00"])
    style SAF fill:#FFC508,color:#fff,stroke:#2b2a33
    SAF(["SAF"])
    style RACF fill:#FFC508,color:#fff,stroke:#2b2a33
    RACF(["RACF"])
    PANELS <--> WRAPPER
    WRAPPER <--> RACFU
    RACFU <--> COREAPI
    COREAPI <--> SAF
    SAF <--> RACF
</pre>
