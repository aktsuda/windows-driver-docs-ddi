---
UID: NF:pep_x.PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE
title: PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE function
author: windows-driver-content
description: The PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE function initializes a platform extension plug-in's (PEP) PEP_ACPI_INTERRUPT_RESOURCE structure.
old-location: kernel\pep_acpi_initialize_interrupt_resource.htm
old-project: kernel
ms.assetid: A89AB86B-4DC9-43ED-9EE6-1D4B693DAB91
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE, PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE function [Kernel-Mode Driver Architecture], kernel.pep_acpi_initialize_interrupt_resource, pepfx/PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pep_x.h
req.include-header: Pep_x.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 10.
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
-	pepfx.h
api_name:
-	PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE
product: Windows
targetos: Windows
req.typenames: PEP_WORK_TYPE, *PPEP_WORK_TYPE, PEP_WORK_TYPE, *PPEP_WORK_TYPE
---


# PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE function
The <b>PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE</b> function initializes a platform extension plug-in's (PEP) <a href="..\pepfx\ns-pepfx-_pep_acpi_interrupt_resource.md">PEP_ACPI_INTERRUPT_RESOURCE</a> structure.

## Syntax

````
FORCEINLINE VOID PEP_ACPI_INITIALIZE_INTERRUPT_RESOURCE(
  _In_  BOOLEAN             ResourceUsage,
  _In_  KINTERRUPT_MODE     EdgeLevel,
  _In_  KINTERRUPT_POLARITY InterruptLevel,
  _In_  BOOLEAN             ShareType,
  _In_  BOOLEAN             Wake,
  _In_  PULONG              PinTable,
  _In_  UCHAR               PinCount,
  _Out_ PPEP_ACPI_RESOURCE  Resource
);
````

## Parameters

`ResourceUsage`

Indicates if this device is in use.

`EdgeLevel`

A <a href="..\wudfwdm\ne-wudfwdm-_kinterrupt_mode.md">KINTERRUPT_MODE</a> enumeration value that identifies the interrupt type.

`InterruptLevel`

A <a href="..\wdm\ne-wdm-_kinterrupt_polarity.md">KINTERRUPT_POLARITY</a> enumeration value that identifies how a device signals an interrupt request on an interrupt line.

`ShareType`

Indicates if the device can be shared.

`Wake`

Indicates if the device can be woken from a low-power state.

`PinTable`

A list of pin numbers on the resource.

`PinCount`

The number of pins described by the <i>PinTable</i> parameter.

`Resource`

A pointer to the resource. The structure behind the pointer is of type <a href="..\pepfx\ns-pepfx-_pep_acpi_interrupt_resource.md">PEP_ACPI_INTERRUPT_RESOURCE</a>.


## Return Value

This function does not return a value.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows version** | Supported starting with Windows 10.  |
| **Target Platform** | Windows |
| **Header** | pep_x.h (include Pep_x.h) |

## See Also

<a href="..\pepfx\ns-pepfx-_pep_acpi_interrupt_resource.md">PEP_ACPI_INTERRUPT_RESOURCE</a>