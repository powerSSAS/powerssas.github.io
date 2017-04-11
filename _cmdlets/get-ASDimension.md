---
title: get-ASDimension
description: Returns a list of Dimensions
layout: cmdlets
---
_**Note**: this cmdlet is not in the current build and at the moment you will need to download the source and compile it yourself._

This cmdlet will get a reference to one or more Dimensions in the specified database/cube.

#### Parameters (by name)
* **ServerName:** the name of the SSAS server.
* **DatabaseName:** the name of the SSAS database.
* **CubeName:** the name of the SSAS cube.
* **DimensionName:** the name of the SSAS dimension.

```poweshell
PS > get-ASDimension localhost "Adventure Works DW" "Adventure Works" Product
```

#### Parameters (by Object)
* **Database:** a SSAS database object.
* **CubeName:** the name of the SSAS Cube
* **DimensionName:** the name of the SSAS Cube

```powershell
PS > get-ASDatabase localhost "Adventure Works DW" | get-ASDimension "Adventure Works" Product
```
