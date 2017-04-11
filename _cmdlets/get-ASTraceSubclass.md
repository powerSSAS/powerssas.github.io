---
title: Get-ASTraceSubclass
description: Returns a list of the Trace Subclasses that are specific to Analysis Services
layout: cmdlets
---
Returns a list of the available event subclasses with their descriptions

### Examples

```powershell
#--------------  List event Subclasses --------------
C:\PS>get-AsTraceSubclass localhost
```
returns a list of the trace subclasses from the localhost server.

```powershell
#--------------  Table of Subclass IDs and Names --------------
    C:\PS>get-AsTraceSubclass localhost | Format-Table EventID, EventName, SubclassID, SubclassName - auto
```

Outputs a table of the Event Sub    classes

### Syntax
``Get-ASTraceSubclass [[-ServerName]([-ServerName) <String>] [<CommonParameters>](_CommonParameters_) }
``

### Parameters
    -ServerName <String>
        The name of the server to query for the trace event subclasses.

        Required?                    false
        Position?                    1
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    <CommonParameters>
        This cmdlet supports the common parameters: -Verbose, -Debug,
        -ErrorAction, -ErrorVariable, and -OutVariable. For more information,
        type, "get-help about_commonparameters".


