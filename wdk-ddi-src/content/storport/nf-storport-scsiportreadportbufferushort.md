---
UID: NF:storport.ScsiPortReadPortBufferUshort
title: ScsiPortReadPortBufferUshort macro
author: windows-driver-content
description: The ScsiPortReadPortBufferUshort routine transfers a given number of USHORT values from the HBA to a buffer.Note  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future.
old-location: storage\scsiportreadportbufferushort.htm
old-project: storage
ms.assetid: b218785c-170e-4a30-99c9-0db8705b7f5d
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: ScsiPortReadPortBufferUshort, ScsiPortReadPortBufferUshort routine [Storage Devices], scsiprt_27acea07-f416-4fa1-894d-6bb38c020f6b.xml, srb/ScsiPortReadPortBufferUshort, storage.scsiportreadportbufferushort
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
-	ScsiPortReadPortBufferUshort
product: Windows
targetos: Windows
req.typenames: STOR_SPINLOCK
req.product: Windows 10 or later.
---


# ScsiPortReadPortBufferUshort function
The <b>ScsiPortReadPortBufferUshort</b> routine transfers a given number of USHORT values from the HBA to a buffer.
<div class="alert"><b>Note</b>  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future. Instead, we recommend using the <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-driver">Storport driver</a> and <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-miniport-drivers">Storport miniport</a> driver models.</div><div> </div>

## Syntax

````
VOID ScsiPortReadPortBufferUshort(
  _In_ PUSHORT Port,
  _In_ PUSHORT Buffer,
  _In_ ULONG   Count
);
````

## Parameters

`Port`

Pointer to the I/O port. The given <i>Port</i> must be in a mapped I/O-space range returned by <b>ScsiPortGetDeviceBase</b>.

`Buffer`

Pointer to the buffer.

`Count`

Specifies the number of USHORT values to read from the HBA.


## Return Value

None

## Remarks

<b>ScsiPortReadPortBufferUshort</b> ensures that the data is transferred correctly.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | storport.h (include Miniport.h, Scsi.h, Storport.h) |
| **Library** | Scsiport.lib |

## See Also

<a href="..\srb\nf-srb-scsiportgetdevicebase.md">ScsiPortGetDeviceBase</a>