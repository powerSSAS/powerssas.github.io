**Project Description**
A PowerShell snapin for SQL Server Analysis Services. It implements a provider with all the interfaces required to enable you to navigate an SSAS server like a drive and includes a number of cmdlets for working with SSAS.

Currently the provider is a fairly thin wrapper over the AMO object model. The aim is to extend the object model to make easy to work with SSAS from the command line and to also add a number of useful cmdlets to make certain tasks easier.

**Introduction to PowerSSAS**
[PowerSSAS release announcement](http://geekswithblogs.net/darrengosbell/archive/2007/11/19/Announcing-the-release-of-PowerSSAS-a-PowerShell-provider-for-Analysis.aspx) - this is currently the best overview of what powerSSAS has to offer.

**Installation Instructions**
The current version comes with a full installer, once it is installed you just need to add the snapin to your session and you are off. The following example will load the provider and create a drive in powershell  called "ssas:" that is connect to the default Analysis Services instance on the localhost.

```powershell
PS > add-pssnapin powerSSAS
PS > new-psdrive ssas powerSSAS localhost 
```

You can then type "ssas:" to navigate to the drive and start using "dir" and "cd" to naviagate around like you would on a file system.

The installer is very simple, but if you have issues installing powerSSAS check out the [Installation Troubleshooting Guide](Installation-Troubleshooting-Guide)

**CmdLets**
||Cmdlet||Description||
|[add-ASAssembly](add-ASAssembly)|Adds an Assembly to an SSAS server or database|
|backup-ASDatabase|Backs-up an SSAS database|
|[clear-ASSession](clear-ASSession)|Clears the specified Session|
|get-asConnection|Returns a list of current connections|
|[get-ASCube](get-ASCube) |Returns a list of Cubes|
|[get-ASCubePermission](get-ASCubePermission)|Returns a set of CubePermissions|
|[get-ASDatabase](get-ASDatabase) |Returns a list of Databases|
|[get-ASDimension](get-ASDimension)* |Returns a list of Dimensions|
|[get-ASLock](get-ASLock) |Returns a list of Locks|
|get-ASRole|Returns a list of Roles|
|[get-ASServer](get-ASServer) |Returns the specified Server object|
|[get-ASSession](get-ASSession)|Lists the current Sessions|
|[get-ASTrace](get-ASTrace)|Returns a list of the current server side traces|
|[get-ASTraceSubclass](get-ASTraceSubclass)|Returns a list of the Trace Subclasses that are specific to Analysis Services|
|[get-ASConnection](get-ASConnection)|Lists the current Connections|
|[invoke-ASDiscover](invoke-ASDiscover)|Executes the specified Discover command against Analysis Services |
|[invoke-ASExecute](invoke-ASExecute)|Executes the specified XMLA command against Analysis Services |
|[invoke-ASMDX](invoke-ASMDX)|Executes the specified MDX command and returns the results |
|[new-ASScript](new-ASScript)|Scripts out a give object to an XMLA Create or Alter script|
|[remove-ASAssembly](remove-ASAssembly)|Removes a specified CLR Assembly|
|restore-ASDatabase|Restores an SSAS Database|
|[send-XmlaDiscover](send-XmlaDiscover)|Sends an Xmla Discover command|

**Example Scripts**
* Getting a list of active sessions
```powershell
PS > get-ASsession localhost 
```
* Getting a list of active connections
```powershell
PS > get-ASconnection localhost 
```

more [Example Scripts](Example-Scripts)

### SQL Server 2008 R2 Support
Initial testing shows that the 2008 version also works against SQL 2008 R2

### Installation

To install PowerSSAS, download the installer from the [Releases](/powerssas/Release/ProjectReleases.aspx) tab.

Or, new as of v 0.3.1.0 you can install PowerSSAS as a PowerShell v2 module. see: [Installing PowerSSAS as a v2 module](Installing-PowerSSAS-as-a-v2-module)

### Suggestions

We are currently in the process of brainstorming other potential features, and have been adding them as [work items](/powerssas/WorkItem/List.aspx). If you have a feature you would like to see added, drop us a line on the [forums](/powerSSAS/Thread/List.aspx).


### Future Releases

The next release date has not yet been scheduled. If you have any requests or issues please use the discussion or issues features on this site.