---
title: Invoke-AsExecute
description: Executes the specified command against Analysis Services
layout: cmdlets
---
Runs an Execute command against the specified server

### Syntax
```
Invoke-AsExecute [[-ServerName]([-ServerName) <String>] [-Xmla](-Xmla) <String> [-WhatIf](-WhatIf) [-Confirm](-Confirm) [<CommonParameters>](_CommonParameters_) }
```

### Parameters
    -ServerName <String>
        The name of the server against which the command should be executed.

        Required?                    false
        Position?                    1
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -Xmla <String>
        The XMLA command to be sent to the server.

        Required?                    true
        Position?                    2
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -WhatIf
        Displays the command that would have been executed without actually executing it.

        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    -Confirm
        Asks for confirmation before executing the specified command

        Required?                    false
        Position?                    named
        Default value
        Accept pipeline input?       false
        Accept wildcard characters?  false

    <CommonParameters>
        This cmdlet supports the common parameters: -Verbose, -Debug,
        -ErrorAction, -ErrorVariable, and -OutVariable. For more information,
        type, "get-help about_commonparameters".