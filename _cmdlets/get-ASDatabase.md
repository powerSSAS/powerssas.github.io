---
title: get-ASDatabase
description: Returns a list of Databases
layout: cmdlets
---
_**Note**: this cmdlet is not in the current build and at the moment you will need to download the source and compile it yourself._

This cmdlet will get a reference to one or more Databases on the specified server

#### Parameters (by name)
* **ServerName:** the name of the SSAS server.
* **DatabaseName:** the name of the SSAS database (will accept wildcards).

```powershell
PS > get-ASDatabase localhost "Adventure Works DW"
```

#### Parameters (by Object)
* **Server:** an SSAS server object, which can be passed in on the pipeline.
* **DatabaseName:** the name of the SSAS server.

```powershell
PS > get-ASServer localhost | get-ASDatabase "Adventure*"
```
