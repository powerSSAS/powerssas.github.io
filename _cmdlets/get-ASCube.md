---
title: get-ASCube
description: Returns a list of Cubes
layout: cmdlets
---

_**Note**: this cmdlet is not in the current build and at the moment you will need to download the source and compile it yourself._

This cmdlet will get a reference to one or more Cubes in the specified database.

#### Parameters (by name)
* **ServerName:** the name of the SSAS server.
* **DatabaseName:** the name of the SSAS database.
* **CubeName:** the name of the SSAS cube.

```powershell
PS > get-ASCube localhost "Adventure Works DW" "Adventure Works"
```

#### Parameters (by Object)
* **Database:** a SSAS database object.
* **CubeName:** the name of the SSAS Cube

```powershell
PS > get-ASDatabase localhost "Adventure Works DW" | get-ASCube "Adventure Works"
```
