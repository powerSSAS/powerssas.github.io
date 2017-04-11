---
title: Installation Troubleshooting Guide
layout: default
---
## Installation Troubleshooting Guide

### Pre-requisites
If you install PowerSSAS on a computer with the SQL Server client tools, you will have everything it needs. If the computer does not have the SQL Server client tools you would need to install the AMO library and ADOMD.NET. (search for the "SQL Server Feature Pack" in your favourite search engine and you should be able to find the downloads for these)

### Installation
There are two stages to the install of PowerSSAS:
 # the files are unpacked and copied to a location on your computer (usuall c:\program files\powerssas)
 # the snapin is registered using the .net installutil utility
I suspect that it is in stage 2. where something has gone wrong. In the install folder there should be some log files created, if there was an issue it should be listed in one of those.

Otherwise you could try running the installutil manually from the command line and see if it prints any error messages

if you navigate to ``"c:\windows\microsoft.net\framework\v2.0.50727"`` and then execute: 

```
installutil "c:\program files\powerssas\powerssas.dll"
```

This should register the snapin, or print an error message if there is an issue. If there are any errors that you can't figure out please post them to the discussions area. If the registration has suceeded you should be able to run **``get-pssnapin -registered``** from a pwershell window and see that powerSSAS is listed. If you can see powerSSAS listed as a registered snapin you should be able to mount drives and use all the cmdlets.
