---
title: Send-XmlaDiscover
description: Sends an Xmla Discover command
layout: cmdlets
---
This cmdlet sends and XMLA discover command to the server and returns the results.

The following command will display a list of all the possible rowsets that you can query

```powershell
PS > send-XmlaDiscover localhost DISCOVER_SCHEMA_ROWSETS
```