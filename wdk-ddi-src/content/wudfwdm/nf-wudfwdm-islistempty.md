---
UID: NF:wudfwdm.IsListEmpty
title: IsListEmpty function
author: windows-driver-content
description: The IsListEmpty routine indicates whether a doubly linked list of LIST_ENTRY structures is empty.
old-location: kernel\islistempty.htm
old-project: kernel
ms.assetid: 6e494112-a808-4914-8194-e68a2799c38e
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: IsListEmpty, IsListEmpty routine [Kernel-Mode Driver Architecture], k109_26969818-30d0-4e01-965d-e0ee6891fdd5.xml, kernel.islistempty, wdm/IsListEmpty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wudfwdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Wudfwdm.h
req.target-type: Desktop
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.irql: Any level (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdm.h
api_name:
-	IsListEmpty
product: Windows
targetos: Windows
req.typenames: PO_FX_PERF_STATE_UNIT, *PPO_FX_PERF_STATE_UNIT
req.product: Windows 10 or later.
---


# IsListEmpty function
The <b>IsListEmpty</b> routine indicates whether a doubly linked list of <a href="https://msdn.microsoft.com/library/windows/hardware/ff554296">LIST_ENTRY</a> structures is empty.

## Syntax

````
BOOLEAN IsListEmpty(
  _In_ const LIST_ENTRY *ListHead
);
````

## Parameters

`ListHead`

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff554296">LIST_ENTRY</a> structure that represents the head of the list.


## Return Value

<b>IsListEmpty</b> returns <b>TRUE</b> if there are currently no entries in the list and <b>FALSE</b> otherwise.

## Remarks

<b>IsListEmpty</b> returns <b>TRUE</b> if <i>ListHead</i>-&gt;<b>Flink</b> refers back to <i>ListHead</i>.

For information about using this routine when implementing a doubly linked list, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563802">Singly and Doubly Linked Lists</a>.

Callers of <b>IsListEmpty</b> can be running at any IRQL. If <b>IsListEmpty</b> is called at IRQL &gt;= DISPATCH_LEVEL, the storage for <i>ListHead</i> must be resident.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows version** | Available starting with Windows 2000.  |
| **Target Platform** | Desktop |
| **Header** | wudfwdm.h (include Wdm.h, Ntddk.h, Ntifs.h, Wudfwdm.h) |
| **IRQL** | Any level (see Remarks section) |

## See Also

<a href="..\wudfwdm\nf-wudfwdm-removetaillist.md">RemoveTailList</a>



<a href="..\wudfwdm\nf-wudfwdm-removeentrylist.md">RemoveEntryList</a>



<a href="..\wudfwdm\nf-wudfwdm-removeheadlist.md">RemoveHeadList</a>



<a href="..\wudfwdm\nf-wudfwdm-initializelisthead.md">InitializeListHead</a>