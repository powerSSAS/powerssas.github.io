Version 2 of Powershell includes the capability of loading up a .dll with compiled cmdlets as a module.

In order to install PowerSSAS as a module you need to have the following pre-requisites:
* AMO (Analysis Management Objects) - this can be downloaded from Microsoft
* PowerShell v2

In order to install PowerSSAS as a module you need to do the following
* create a "PowerSSAS" folder in one of your modules folders (which default to the following locations
	* current user: _<documents>_\WindowsPowerShell\modules
	* everyone: c:\windows\system32\WindowsPowerShell\v1.0\Modules
* download one of the module .zip files
* unzip the module into this new folder you just created
* type the following from a PowerShell session to include PowerSSAS in your current runspace
```powershell
 import-module powerSSAS
```