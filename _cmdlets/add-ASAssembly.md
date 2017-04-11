---
title: add-ASAssembly
description: Adds an Assembly to an SSAS server or database
layout: cmdlets
---

Adds a CLR assembly to the specified server or database}

### Parameters

-AssemblyName <String>
    This is the Name which the assembly is known by in Analysis Services
    
    Required?                    true
    Position?                    1
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-FilePath <String>
    This is the path and file name of the .dll file for the assembly
    
    Required?                    true
    Position?                    2
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-PermissionSet <PermissionSet>
    
    
    Required?                    true
    Position?                    3
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-Database <Database>
    This is the Database object to which you want to add the assembly
    
    Required?                    false
    Position?                    4
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-DatabaseName <String>
    If the assembly is to be loaded under a particular database you can specify it's name with this parameter.
    
    Required?                    false
    Position?                    5
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-Server <Server>
    This is the server object for where the assembly is to be loaded. You can either use pass in a server object or use
     the ServerName parameter.
    
    Required?                    false
    Position?                    4
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    

-ServerName <String>
    This is the name of the server to which the assembly is to be loaded. You can either use this parameter or pass a S
    erver object to the Server parameter.
    
    Required?                    true
    Position?                    4
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    



