---
UID: NF:wdtfpnpaction.IWDTFPNPAction2.EDTCancelRemoveDevice
title: IWDTFPNPAction2::EDTCancelRemoveDevice method
author: windows-driver-content
description: Sends an IRP_MN_CANCEL_REMOVE_DEVICE event to the target device.
old-location: dtf\iwdtfpnpaction2_edtcancelremovedevice.htm
old-project: dtf
ms.assetid: d3175850-556b-41bd-9b99-225ca3238b25
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: EDTCancelRemoveDevice method [Windows Device Testing Framework], EDTCancelRemoveDevice method [Windows Device Testing Framework], IWDTFPNPAction2 interface, EDTCancelRemoveDevice,IWDTFPNPAction2.EDTCancelRemoveDevice, IWDTFPNPAction2, IWDTFPNPAction2 interface [Windows Device Testing Framework], EDTCancelRemoveDevice method, IWDTFPNPAction2::EDTCancelRemoveDevice, Microsoft.WDTF.IWDTFPNPAction2.EDTCancelRemoveDevice, Microsoft::WDTF::IWDTFPNPAction2::EDTCancelRemoveDevice, dtf.iwdtfpnpaction2_edtcancelremovedevice, wdtfpnpaction/IWDTFPNPAction2::EDTCancelRemoveDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfpnpaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFPNPAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFDriverPNPAction.Interop.dll
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
-	WDTFDriverPNPAction.Interop.dll
api_name:
-	IWDTFPNPAction2.EDTCancelRemoveDevice
product: Windows
targetos: Windows
req.typenames: TTraceLevel
req.product: Windows 10 or later.
---


# EDTCancelRemoveDevice method
Sends an IRP_MN_CANCEL_REMOVE_DEVICE event to the target device.

## Syntax

````
HRESULT EDTCancelRemoveDevice(
  [out, retval] VARIANT_BOOL *pbSuccess
);
````

## Parameters

`pbSuccess`

True if the operation succeeds; otherwise, false.


## Return Value

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## Remarks

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/8fc225af-09d4-42a0-a862-4af89addd5f8">IWDTFEnhancedDeviceTestSupportAction2::Enable</a>  
method must be called for the target device before calling this method.</div>
<div> </div>
<b>EDTCancelRemoveDevice</b> triggers an IRP_MN_CANCEL_REMOVE event
by intentionally failing an IRP_MN_QUERY_REMOVE_DEVICE event.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows version** | Windows XP Professional Windows Server 2008 |
| **Target Platform** | Desktop |
| **Header** | wdtfpnpaction.h |

## See Also

<a href="..\wdtfpnpaction\nn-wdtfpnpaction-iwdtfpnpaction2.md">IWDTFPNPAction2</a>