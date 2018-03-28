---
UID: NE:srb._STOR_DEVICE_POWER_STATE
title: "_STOR_DEVICE_POWER_STATE"
author: windows-driver-content
description: The STOR_DEVICE_POWER_STATE enumerator specifies a device power state.
old-location: storage\stor_device_power_state.htm
old-project: storage
ms.assetid: 563ece3e-1359-4e3c-9ae7-61b94bf90ad0
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PSTOR_DEVICE_POWER_STATE, PSTOR_DEVICE_POWER_STATE, PSTOR_DEVICE_POWER_STATE enumeration pointer [Storage Devices], STOR_DEVICE_POWER_STATE, STOR_DEVICE_POWER_STATE enumeration [Storage Devices], StorPowerDeviceD0, StorPowerDeviceD1, StorPowerDeviceD2, StorPowerDeviceD3, StorPowerDeviceMaximum, StorPowerDeviceUnspecified, _STOR_DEVICE_POWER_STATE, storage.stor_device_power_state, storport/PSTOR_DEVICE_POWER_STATE, storport/STOR_DEVICE_POWER_STATE, storport/StorPowerDeviceD0, storport/StorPowerDeviceD1, storport/StorPowerDeviceD2, storport/StorPowerDeviceD3, storport/StorPowerDeviceMaximum, storport/StorPowerDeviceUnspecified, structs-storport_1b3e3040-821f-4cc1-9a5b-15ae5eaeb35e.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: srb.h
req.include-header: Storport.h, Minitape.h, Srb.h
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
-	HeaderDef
api_location:
-	storport.h
api_name:
-	STOR_DEVICE_POWER_STATE
product: Windows
targetos: Windows
req.typenames: STOR_DEVICE_POWER_STATE, *PSTOR_DEVICE_POWER_STATE
req.product: Windows 10 or later.
---

# _STOR_DEVICE_POWER_STATE Enumeration
The STOR_DEVICE_POWER_STATE enumerator specifies a device power state.

## Syntax
````
typedef enum _STOR_DEVICE_POWER_STATE { 
  StorPowerDeviceUnspecified  = 0,
  StorPowerDeviceD0           = 1,
  StorPowerDeviceD1           = 2,
  StorPowerDeviceD2           = 3,
  StorPowerDeviceD3           = 4,
  StorPowerDeviceMaximum      = 5
} STOR_DEVICE_POWER_STATE, *PSTOR_DEVICE_POWER_STATE;
````

## Constants

<table>
            
                <tr>
                    <td>StorPowerDeviceUnspecified</td>
                    <td>Device power state unspecified.</td>
                </tr>
            
                <tr>
                    <td>StorPowerDeviceD0</td>
                    <td>The D0 device power state.</td>
                </tr>
            
                <tr>
                    <td>StorPowerDeviceD1</td>
                    <td>The D1 device power state.</td>
                </tr>
            
                <tr>
                    <td>StorPowerDeviceD2</td>
                    <td>The D2 device power state.</td>
                </tr>
            
                <tr>
                    <td>StorPowerDeviceD3</td>
                    <td>The D3 device power state.</td>
                </tr>
            
                <tr>
                    <td>StorPowerDeviceMaximum</td>
                    <td>The upper delimiting value on device power states.</td>
                </tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | srb.h (include Storport.h, Minitape.h, Srb.h) |

## See Also

<a href="..\storport\ns-storport-_scsi_power_request_block.md">SCSI_POWER_REQUEST_BLOCK</a>