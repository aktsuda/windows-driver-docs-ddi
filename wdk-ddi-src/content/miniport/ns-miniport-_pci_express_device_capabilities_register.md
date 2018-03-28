---
UID: NS:miniport._PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER
title: "_PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER"
author: windows-driver-content
description: The PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER structure describes a PCI Express (PCIe) device capabilities register of a PCIe capability structure.
old-location: pci\pci_express_device_capabilities_register.htm
old-project: PCI
ms.assetid: 895b49e5-181b-4312-ab1c-7f67c102b32f
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PPCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER, PCI.pci_express_device_capabilities_register, PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER, PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER union [Buses], PPCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER, PPCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER union pointer [Buses], _PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER, ntddk/PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER, ntddk/PPCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER, pci_struct_6643c57c-39dd-483b-9611-b0bf96cacbd8.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: miniport.h
req.include-header: Ntddk.h, Miniport.h
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
req.irql: Any level (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddk.h
api_name:
-	PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER
product: Windows
targetos: Windows
req.typenames: PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER, *PPCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER
---

# _PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER structure
The PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER structure describes a PCI Express (PCIe) device capabilities register of a PCIe capability structure.

## Syntax
````
typedef union _PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER {
  struct {
    ULONG MaxPayloadSizeSupported  :3;
    ULONG PhantomFunctionsSupported  :2;
    ULONG ExtendedTagSupported  :1;
    ULONG L0sAcceptableLatency  :3;
    ULONG L1AcceptableLatency  :3;
    ULONG Undefined  :3;
    ULONG RoleBasedErrorReporting  :1;
    ULONG Rsvd1  :2;
    ULONG CapturedSlotPowerLimit  :8;
    ULONG CapturedSlotPowerLimitScale  :2;
    ULONG Rsvd2  :4;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER, *PPCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER;
````

## Members


`DUMMYSTRUCTNAME`



`AsULONG`

A ULONG representation of the contents of the PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER structure.

## Remarks
The PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_DEVICE_CAPABILITIES_REGISTER structure is contained in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537460">PCI_EXPRESS_CAPABILITY</a> structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | miniport.h (include Ntddk.h, Miniport.h) |

## See Also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537460">PCI_EXPRESS_CAPABILITY</a>