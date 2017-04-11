---
title:  Get-ASTrace
description: Returns a list of the current server side traces
layout: cmdlets
---
Returns a collection of trace objects from the server

### Syntax
```
Get-ASTrace [[-XmlaRestrictions]([-XmlaRestrictions) <AdomdRestrictionCollection>] [[-DatabaseName]([-DatabaseName) <String>] [[-ServerName]([-ServerName) <String>] [<CommonParameters>](_CommonParameters_) 

Get-ASTrace [[-ASServer]([-ASServer) <Server>] [<CommonParameters>](_CommonParameters_)```


### Parameters
    -XmlaRestrictions <AdomdRestrictionCollection>
        Required?                    false
        Position?                    2
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -DatabaseName <String>
        Required?                    false
        Position?                    3
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -ServerName <String>
        The name of the server from which to get the list of server side Traces

        Required?                    false
        Position?                    1
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -ASServer <Server>
        Required?                    false
        Position?                    1
        Default value
        Accept pipeline input?       true (ByValue)
        Accept wildcard characters?  false

    <CommonParameters>
        This cmdlet supports the common parameters: -Verbose, -Debug,
        -ErrorAction, -ErrorVariable, and -OutVariable. For more information,
        type, "get-help about_commonparameters".