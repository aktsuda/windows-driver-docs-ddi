---
UID: NF:wdtf.IWDTFTargets2.Add
title: IWDTFTargets2::Add method
author: windows-driver-content
description: Add a single item to the collection.
old-location: dtf\iwdtftargets2_add.htm
old-project: dtf
ms.assetid: 0d8ba3ae-3afd-4f26-9951-0d4bdc9e4d49
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: Add method [Windows Device Testing Framework], Add method [Windows Device Testing Framework], IWDTFTargets2 interface, Add,IWDTFTargets2.Add, IWDTFTargets2, IWDTFTargets2 interface [Windows Device Testing Framework], Add method, IWDTFTargets2::Add, Microsoft.WDTF.IWDTFTargets2.Add, Microsoft::WDTF::IWDTFTargets2::Add, dtf.iwdtftargets2_add, wdtf/IWDTFTargets2::Add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtf.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTF.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTF.Interop.metadata_dll
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
-	WDTF.Interop.metadata_dll.dll
api_name:
-	IWDTFTargets2.Add
product: Windows
targetos: Windows
req.typenames: TTraceLevel
req.product: Windows 10 or later.
---


# Add method
Add a single item to the collection.

## Syntax

````
HRESULT Add(
  [in] IWDTFTarget2 *pTarget
);
````

## Parameters

`pTarget`

The item to add to this collection.


## Return Value

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows version** | Windows XP Professional Windows Server 2008 |
| **Target Platform** | Desktop |
| **Header** | wdtf.h |

## See Also

<a href="..\wdtf\nn-wdtf-iwdtftargets2.md">IWDTFTargets2</a>