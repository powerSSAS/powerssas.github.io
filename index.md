---
layout: default
title: "powerSSAS"
---


powerSSAS is a PowerShell snapin for SQL Server Analysis Services. It implements a provider with all the interfaces required to enable you to navigate an SSAS server like a drive and includes a number of cmdlets for working with SSAS.

Currently the provider is a fairly thin wrapper over the AMO object model. The aim is to extend the object model to make easy to work with SSAS from the command line and to also add a number of useful cmdlets to make certain tasks easier.

# Introduction to PowerSSAS
[PowerSSAS release announcement](http://geekswithblogs.net/darrengosbell/archive/2007/11/19/Announcing-the-release-of-PowerSSAS-a-PowerShell-provider-for-Analysis.aspx) - this is currently the best overview of what powerSSAS has to offer.

# Installation Instructions
The current version comes with a full installer, once it is installed you just need to add the snapin to your session and you are off. The following example will load the provider and create a drive in powershell  called "ssas:" that is connect to the default Analysis Services instance on the localhost.

```powershell
PS > add-pssnapin powerSSAS
PS > new-psdrive ssas powerSSAS localhost 
```

You can then type "ssas:" to navigate to the drive and start using "dir" and "cd" to naviagate around like you would on a file system.

The installer is very simple, but if you have issues installing powerSSAS check out the [Installation Troubleshooting Guide](Installation-Troubleshooting-Guide)

### Alternative Installation as a Module
As of v 0.3.1.0 you can install PowerSSAS as a PowerShell v2 module. see: [Installing PowerSSAS as a v2 module](Installing-PowerSSAS-as-a-v2-module)

# Features
  
| Cmdlet | Description |
|:-------|:------------|
{% for cmdlet in site.cmdlets %}| [{{ cmdlet.title }}]({{ cmdlet.url }}) | {{ cmdlet.description }} |
{% endfor %}

# Examples

{% for ex in site.examples %}* [{{ ex.title }}]({{ ex.url }})
{% endfor %}
