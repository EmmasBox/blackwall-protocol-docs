---
layout: page
nav_exclude: false
---

# Dependencies

## Required dependencies

### System dependencies

- z/OS 2.5 or later.
- OpenSSH installed and configured on z/OS (for connecting to z/OS UNIX)
  - OMVS in ISPF does not work due to a lack of terminal features.
- Python 3.12 or later.

### Python packages

- Textual 3.1.0 or later (for UI)
- [RACFU](https://github.com/ambitus/racfu) (To communicate with RACF)
  - RACFU being a dependency means you need the IRRSEQ00, IRRSMO00 and RACF Subsystem Address Space configured.

## Optional dependencies

### Python packages

- [ZOAU 1.3.4.x or later](https://www.ibm.com/docs/en/zoau/1.3.x) (For gathering system information like LPAR name. Not required but highly recommended)
- [textual-image](https://github.com/lnqs/textual-image), [pillow](https://github.com/python-pillow/Pillow), and [zlib](https://github.com/zopencommunity/zlibport) (For image support)
