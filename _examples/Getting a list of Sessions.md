---
title: Getting a List of Sessions
layout: example
---
At the simplest level you can either call the get-ASSession cmdlet

```powershell
PS > add-pssnapin powerSSAS # this only needs to be run once per session
PS > get-ASSession localhost 
```

This can be run from any location (provided you have powerSSAS [Loaded](Adding-the-powerSSAS-snapin)

Or if you have [created a drive](Creating-a-drive) then you can navigate to the sessions collection

```powershell
PS > add-pssnapin powerSSAS
PS > new-psdrive ssas powerSSAS localhost
PS > ssas:
PS > cd sessions
PS > dir
```

