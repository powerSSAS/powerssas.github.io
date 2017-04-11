---
title: get&#8209;ASCubePermission
description: Returns a set of CubePermissions
layout: cmdlets
---
Returns the CubePermissions for the specified Role.

```powershell
#--------------  Get CubePermissions for a role -------------- 
$role = get-asrole -servername "localhost\sql08" -databasename "adventure works dw 2008" -RoleName Test 
get-ascubepermission -RoleObject $role
```

### Parameters

-RoleObject <Role>
    This is the role for which the CubePermissions are to be listed
    
    Required?                    false
    Position?                    named
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  false
    
### See Also
[get-ASRole](get-ASRole)