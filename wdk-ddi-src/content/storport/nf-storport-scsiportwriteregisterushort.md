---
UID: NF:storport.ScsiPortWriteRegisterUshort
title: ScsiPortWriteRegisterUshort macro
author: windows-driver-content
description: The ScsiPortWriteRegisterUshort routine transfers a USHORT value to the HBA.Note  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future.
old-location: storage\scsiportwriteregisterushort.htm
old-project: storage
ms.assetid: a6ed2bb8-e62c-4566-9b61-6acac68e8309
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: ScsiPortWriteRegisterUshort, ScsiPortWriteRegisterUshort routine [Storage Devices], scsiprt_550ba014-1ffa-496f-8cea-009f234fa8e4.xml, srb/ScsiPortWriteRegisterUshort, storage.scsiportwriteregisterushort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: storport.h
req.include-header: Miniport.h, Scsi.h, Storport.h
req.target-type: Desktop
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
req.lib: Scsiport.lib
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Scsiport.lib
-	Scsiport.dll
api_name:
-	ScsiPortWriteRegisterUshort
product: Windows
targetos: Windows
req.typenames: STOR_SPINLOCK
req.product: Windows 10 or later.
---


# ScsiPortWriteRegisterUshort function
The <b>ScsiPortWriteRegisterUshort</b> routine transfers a USHORT value to the HBA.
<div class="alert"><b>Note</b>  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future. Instead, we recommend using the <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-driver">Storport driver</a> and <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-miniport-drivers">Storport miniport</a> driver models.</div><div> </div>

## Syntax

````
VOID ScsiPortWriteRegisterUshort(
  _In_ PUSHORT Register,
  _In_ USHORT  Value
);
````

## Parameters

`Register`

Pointer to the register. The given <i>Register</i> must be in a mapped memory-space range returned by <b>ScsiPortGetDeviceBase</b>.

`Value`

Specifies the value to be written to the HBA's register.


## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | storport.h (include Miniport.h, Scsi.h, Storport.h) |
| **Library** | Scsiport.lib |

## See Also

<a href="..\srb\nf-srb-scsiportgetdevicebase.md">ScsiPortGetDeviceBase</a>