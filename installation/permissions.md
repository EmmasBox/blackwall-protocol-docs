---
layout: default
parent: Interfaces
---

# Required permissions

Make sure each user that is supposed to use this software has access to the following RACF profiles:

 Class    | Profile                  | Access | Reason
----------|--------------------------|--------|--------
 FACILITY | IRR.RADMIN.LISTUSER      | Read   | User information
 FACILITY | IRR.RADMIN.LISTGRP       | Read   | Group information
 FACILITY | IRR.RADMIN.RLIST         | Read   | General resource profile information
 FACILITY | IRR.RADMIN.LISTDSD       | Read   | Dataset profile information
 FACILITY | IRR.RADMIN.SETROPTS.LIST | Read   | RACF system settings
 XFACILIT | IRR.IRRSMO00.PRECHECK    | Read   | Create new profiles in RACF and modify things

It is suggested to create a group with each of the required resources. This group can be named "BLACKWAL" after the program.

## Notes

These permissions allow users of Blackwall access to IRRSMO00 and IRRSEQ00, which respectively allow users to interact with RACF and pull data out of RACF. Do not give these accesses to people aren't authorized to work with security.
