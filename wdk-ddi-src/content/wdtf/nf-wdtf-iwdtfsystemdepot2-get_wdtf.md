---
UID: NF:wdtf.IWDTFSystemDepot2.get_WDTF
title: IWDTFSystemDepot2::get_WDTF method
author: windows-driver-content
description: Gets the main WDTF aggregation object.
old-location: dtf\iwdtfdevicedepot2_wdtf.htm
old-project: dtf
ms.assetid: 911e5f2b-bd8c-42e6-8272-a447e723e814
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: IWDTFDeviceDepot2 interface [Windows Device Testing Framework], WDTF property, IWDTFDeviceDepot2.WDTF, IWDTFDeviceDepot2::get_WDTF, IWDTFSystemDepot2, IWDTFSystemDepot2::get_WDTF, Microsoft.WDTF.IWDTFDeviceDepot2.WDTF, Microsoft::WDTF::IWDTFDeviceDepot2::WDTF, WDTF property [Windows Device Testing Framework], WDTF property [Windows Device Testing Framework], IWDTFDeviceDepot2 interface, dtf.iwdtfdevicedepot2_wdtf, get_WDTF,IWDTFSystemDepot2.get_WDTF, wdtf/IWDTFDeviceDepot2::WDTF, wdtf/IWDTFDeviceDepot2::get_WDTF
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtf.h
req.include-header: 
req.target-type: Windows
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
-	IWDTFDeviceDepot2.WDTF
-	IWDTFDeviceDepot2.get_WDTF
product: Windows
targetos: Windows
req.typenames: TTraceLevel
req.product: Windows 10 or later.
---


# get_WDTF method
Gets the main WDTF aggregation object.

This property is read-only.

## Syntax

````
HRESULT get_WDTF(
  [out, retval] IWDTF2 **ppWDTF
);
````

## Parameters

`ppWDTF`




## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows version** | Windows XP Professional Windows Server 2008 |
| **Target Platform** | Windows |
| **Header** | wdtf.h |

## See Also

<a href="..\wdtf\nn-wdtf-iwdtf2.md">IWDTF2</a>



<a href="..\wdtf\nn-wdtf-iwdtfdevicedepot2.md">IWDTFDeviceDepot2</a>