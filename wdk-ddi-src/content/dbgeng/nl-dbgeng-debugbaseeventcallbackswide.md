---
UID: NL:dbgeng.DebugBaseEventCallbacksWide
title: DebugBaseEventCallbacksWide
author: windows-driver-content
description: The DebugBaseEventCallbacksWide class provides a base implementation of the IDebugEventCallbacksWide interface.
old-location: debugger\debugbaseeventcallbackswide.htm
old-project: debugger
ms.assetid: 38AD8472-1BA3-42EA-99CE-E91098A5B334
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DebugBaseEventCallbacksWide, DebugBaseEventCallbacksWide class [Windows Debugging], DebugBaseEventCallbacksWide class [Windows Debugging], described, dbgeng/DebugBaseEventCallbacksWide, debugger.debugbaseeventcallbackswide
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dbgeng.h
api_name:
-	DebugBaseEventCallbacksWide
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# DebugBaseEventCallbacksWide Class
The <b>DebugBaseEventCallbacksWide</b> class provides a base implementation
of the <a href="..\dbgeng\nn-dbgeng-idebugeventcallbackswide.md">IDebugEventCallbacksWide</a> interface.  

A program can derive an event callbacks class from <b>DebugBaseEventCallbacksWide</b> and implement
only the methods needed. 

Be careful to implement <a href="https://msdn.microsoft.com/b1e62ae3-4a3d-42db-b7fe-87d1a7e0b438">GetInterestMask</a> appropriately.

## Methods

<p>The <b>DebugBaseEventCallbacksWide</b> class has these methods.</p>

| Method | Description |
| ---- |:---- |


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Windows |
| **Header** | dbgeng.h (include Dbgeng.h) |

## See Also

<a href="..\dbgeng\nn-dbgeng-idebugeventcallbackswide.md">IDebugEventCallbacksWide</a>



<a href="https://msdn.microsoft.com/b1e62ae3-4a3d-42db-b7fe-87d1a7e0b438">GetInterestMask</a>