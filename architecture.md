---
layout: default
title: Architecture
has_toc: false
---

# Architecture of Blackwall

<pre class="mermaid">
    flowchart TD
        Blackwall command line--> TSOCMD
        TSOCMD -->z/OS
        Blackwall UI panels -->Blackwall API wrapper
        Blackwall API wrapper -->RACFU
        RACFu -->SAF(SAF)
        SAF -->RACF[(RACF)]
</pre>
