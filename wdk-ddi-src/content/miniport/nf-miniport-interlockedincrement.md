---
UID: NF:miniport.InterlockedIncrement
title: InterlockedIncrement function
author: windows-driver-content
description: The InterlockedIncrement routine increments a caller-supplied variable as an atomic operation.
old-location: kernel\interlockedincrement.htm
old-project: kernel
ms.assetid: e8f4c3c9-c5b7-4fc1-9be3-0254c6cbd6f3
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: InterlockedIncrement, InterlockedIncrement routine [Kernel-Mode Driver Architecture], k102_8d625992-2e36-464d-a771-629d5f08b398.xml, kernel.interlockedincrement, wdm/InterlockedIncrement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: miniport.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
req.target-type: Universal
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
req.lib: OneCoreUAP.lib on Windows 10
req.dll: 
req.irql: Any level
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OneCoreUAP.lib
-	OneCoreUAP.dll
-	API-MS-Win-Core-Interlocked-l1-1-0.dll
-	API-MS-Win-Core-Interlocked-l1-2-0.dll
-	KernelBase.dll
-	MinKernelBase.dll
api_name:
-	InterlockedIncrement
product: Windows
targetos: Windows
req.typenames: MEMORY_CACHING_TYPE
---


# InterlockedIncrement function
The <b>InterlockedIncrement</b> routine increments a caller-supplied variable as an atomic operation.

## Syntax

````
LONG InterlockedIncrement(
  _Inout_ LONG volatile *Addend
);
````

## Parameters

`Addend`

A pointer to a variable of type LONG.


## Return Value

<b>InterlockedIncrement</b> returns the incremented value.

## Remarks

<b>InterlockedIncrement</b> should be used instead of <b>ExInterlockedIncrementLong</b> because it is both more efficient and faster. 

<b>InterlockedIncrement </b>is implemented inline by the compiler when appropriate and possible. It does not require a spin lock and can therefore be safely used on pageable data.

<b>InterlockedIncrement</b> is atomic only with respect to other <b>Interlocked<i>Xxx</i></b> calls. 

Interlocked operations cannot be used on non-cached memory.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows version** | Available starting with Windows 2000.  |
| **Target Platform** | Universal |
| **Header** | miniport.h (include Wdm.h, Ntddk.h, Ntifs.h, Miniport.h) |
| **Library** | OneCoreUAP.lib on Windows 10 |
| **IRQL** | Any level |

## See Also

<a href="..\wdm\nf-wdm-interlockedexchange.md">InterlockedExchange</a>



<a href="..\wdm\nf-wdm-exinterlockedaddlargeinteger.md">ExInterlockedAddLargeInteger</a>



<a href="..\wdm\nf-wdm-interlockeddecrement.md">InterlockedDecrement</a>



<a href="..\wdm\nf-wdm-exinterlockedaddulong.md">ExInterlockedAddUlong</a>