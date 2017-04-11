---
title: Invoke-AsMdx
description: Executes the specified MDX command against Analysis Services
layout: cmdlets
---

    Executes an MDX statement and returns the result as a collection of PSObjects

### Examples
    --------------  Simple Query --------------

```powershell
C:\PS>Invoke-AsMdx localhost "Adventure Works DW" "SELECT [Measures](Measures).[Internet Sales Amount](Internet-Sales-Amount) on 0 FROM [Adventure Works](Adventure-Works)"
```

### Syntax
``
Invoke-ASMDX [-Query](-Query) <String> [-ServerName](-ServerName) <String> [-DatabaseName](-DatabaseName) <String> [<CommonParameters>](_CommonParameters_) }
``

### Parameters
    -Query <String>
        A string containing an MDX query

        Required?                    true
        Position?                    3
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -ServerName <String>
        The name of the server against which the query is to be executed.

        Required?                    true
        Position?                    1
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -DatabaseName <String>
        The name of the database against which the query should be executed.

        Required?                    true
        Position?                    2
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    <CommonParameters>
        This cmdlet supports the common parameters: -Verbose, -Debug,
        -ErrorAction, -ErrorVariable, and -OutVariable. For more information,
        type, "get-help about_commonparameters".