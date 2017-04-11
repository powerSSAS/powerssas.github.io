---
title: Invoke-AsDiscover
description: Executes the specified Discover command against Analysis Services
layout: cmdlets
---
Returns the results from the specified DISCOVER command

### Examples


 Calling DISCOVER_CONNECTIONS

```powershell
C:\PS>invoke-asdiscover localhost\sql08 DISCOVER_CONNECTIONS | ft
```


### Syntax
```
Invoke-AsDiscover [-ServerName](-ServerName) <String> [-RowsetName](-RowsetName) <String> [-Restrictions <AdomdRestrictionCollection>](-Restrictions-_AdomdRestrictionCollection_) [-Properties <String>](-Properties-_String_) [-WhatIf](-WhatIf) [-Confirm](-Confirm) [<CommonParameters>](_CommonParameters_) 
```

### See Also
The following cmdlets provide an easy way to execute some of the more common discover requests.

* [get-ASConnection](get-ASConnection)
* [get-ASLock](get-ASLock)
* [get-ASSession](get-ASSession)
* [get-ASTrace](get-ASTrace)

### Parameters
    -ServerName <String>
        The server against which to execute the DISCOVER

        Required?                    true
        Position?                    1
        Default value
        Accept pipeline input?       true (ByValue)
        Accept wildcard characters?  false

    -RowsetName <String>
        The Schema rowset which is to be executed by the Discover command

        Required?                    true
        Position?                    2
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -Restrictions <AdomdRestrictionCollection>
        An XMLA snippet containing the restrictions that apply to the specified rowset.

        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -Properties <String>
        An XMLA snippet containing the properties that apply to the specified rowset.

        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -WhatIf
        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -Confirm
        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    <CommonParameters>
        This cmdlet supports the common parameters: -Verbose, -Debug,
        -ErrorAction, -ErrorVariable, and -OutVariable. For more information,
        type, "get-help about_commonparameters".



