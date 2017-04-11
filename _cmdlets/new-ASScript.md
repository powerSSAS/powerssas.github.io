---
title: New-ASScript
description: Scripts out a give object to an XMLA Create or Alter script
layout: cmdlets
---

Generates an XMLA script for the specified object.

### Syntax
  New-ASScript [-Create](-Create) [-InputObject](-InputObject) <MajorObject> [-ExcludeDependents](-ExcludeDependents) [-ExcludePermissions](-ExcludePermissions) [-ExcludePartitions](-ExcludePartitions)  [<CommonParameters>](_CommonParameters_) 


### Examples
    --------------  Get a Dimension XMLA alter script --------------

```powershell
    C:\PS>$dim = get-AsDimension localhost\sql08 "Adventure Works DW 2008" "Geography"
    $script = new-AsScript $dim
```
Returns the XMLA Alter script as a string to the $script variable


    --------------  Create an Xmla File --------------

```powershell
    C:\PS>get-AsDimension localhost\sql08 "Adventure Works DW 2008" "Geography" | new-AsScript $dim > c:\data\DimGeography.xmla
```

This script pipes the output of the new-AsScript cmdlet to the DimGeography.xmla file.

### Parameters
    -Create
        Setting this flag Will cause the cmdlet to return a CREATE script instead of an ALTER script.

        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -InputObject <MajorObject>
        This is the object for which the XMLA script will be generated

        Required?                    true
        Position?                    1
        Default value
        Accept pipeline input?       true (ByValue)
        Accept wildcard characters?  false

    -ExcludeDependents
        Excludes dependant objects only scripting the specified object

        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -ExcludePermissions
        Excludes permissions from the XMLA script

        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -ExcludePartitions
        Excludes partitions from a Cube script

        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    <CommonParameters>
        This cmdlet supports the common parameters: -Verbose, -Debug,
        -ErrorAction, -ErrorVariable, and -OutVariable. For more information,
        type, "get-help about_commonparameters".

