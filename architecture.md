---
layout: default
title: Architecture
has_toc: false
---

# Architecture of Blackwall

Below you can see a simplified architecture flowchart

<pre class="mermaid">
flowchart TD
    BLACKWALL(["Blackwall program"])
    PYTHON(["Python"])
    TEXTUAL(["Textual application"])
    BLACKWALL --> TEXTUAL
    BLACKWALL --- PYTHON
    TEXTUAL --> COMMANDLINE
    PYTHON --- TEXTUAL

    TABS(["Tab system"])
    TEXTUAL --> TABS
    TABS --> PANELS

    BLACKWALLSCREENS(["Blackwall screens"])
    TEXTUAL --> BLACKWALLSCREENS

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

    PANELS(["Blackwall tab panels"])
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
