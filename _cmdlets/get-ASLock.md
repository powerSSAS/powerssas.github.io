---
title: get-ASLock
description: Returns a list of Locks
layout: cmdlets
---

_**Note**: this cmdlet is not in the current build and at the moment you will need to download the source and compile it yourself._

This cmdlet will return a list of locks.

#### Parameters (by name)
* **ServerName:** the name of the SSAS server.
* **WRITE_LOCK:** returns write locks which are taken during processing.
* **READ_LOCK:** returns read locks which are taken during processing.
* **WAITING:** returns locks which are waiting to be granted.
* **GRANTED:** returns locks which have been granted.
* **SPID:** returns locks which relate to the specified SPID.
* **TransactionID:** returns locks which relate to the specified Transaction.
* **MinimumMS:** returns locks which have been active for at least the specified number of milliseconds.

```powershell
PS > get-ASLock localhost -WRITE_LOCK
```

