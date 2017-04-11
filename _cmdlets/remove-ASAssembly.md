---
title: Remove&#8209;ASClrAssembly
description: Removes a specified CLR Assembly
layout: cmdlets
---

Removes the specified CLR Assembly from Analysis Services


### Parameters

-AssemblyName <String>
    The name of the Assembly to remove
    
    Required?                    true
    Position?                    1
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-DatabaseName <String>
    The name of the Database if this is a database level assembly that is being removed.
    
    Required?                    false
    Position?                    2
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-ServerName <String>
    The name of the server where the assembly is stored.
    
    Required?                    false
    Position?                    3
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-WhatIf 
    Specifying -WhatIf will print a message of what the command would have done, but will not actually perform the acti
    on.
    
    Required?                    false
    Position?                    named
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-Confirm 
    Will request confirmation before dropping any assemblies
    
    Required?                    false
    Position?                    named
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-Server <Server>
    The server object from which to remove the assembly
    
    Required?                    false
    Position?                    2
    Default value                
    Accept pipeline input?       true (ByValue)
    Accept wildcard characters?  false
    

-Database <Database>
    The database object from which to remove the assembly
    
    Required?                    false
    Position?                    2
    Default value                
    Accept pipeline input?       true (ByValue)
    Accept wildcard characters?  false
