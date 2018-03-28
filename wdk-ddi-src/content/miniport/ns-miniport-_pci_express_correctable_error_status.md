---
UID: NS:miniport._PCI_EXPRESS_CORRECTABLE_ERROR_STATUS
title: "_PCI_EXPRESS_CORRECTABLE_ERROR_STATUS"
author: windows-driver-content
description: The PCI_EXPRESS_CORRECTABLE_ERROR_STATUS structure describes a PCI Express (PCIe) correctable error status register of a PCIe advanced error reporting capability structure.
old-location: pci\pci_express_correctable_error_status.htm
old-project: PCI
ms.assetid: 24d10f3a-5188-4dda-8e4e-1dc7ae2ddc88
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PPCI_CORRECTABLE_ERROR_STATUS, PCI.pci_express_correctable_error_status, PCI_EXPRESS_CORRECTABLE_ERROR_STATUS, PCI_EXPRESS_CORRECTABLE_ERROR_STATUS union [Buses], PPCI_CORRECTABLE_ERROR_STATUS, PPCI_CORRECTABLE_ERROR_STATUS union pointer [Buses], _PCI_EXPRESS_CORRECTABLE_ERROR_STATUS, pci_struct_1366a090-7405-4cd8-b725-19753a248441.xml, wdm/PCI_EXPRESS_CORRECTABLE_ERROR_STATUS, wdm/PPCI_CORRECTABLE_ERROR_STATUS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: miniport.h
req.include-header: Ntddk.h, Wdm.h, Miniport.h
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
-	wdm.h
api_name:
-	PCI_EXPRESS_CORRECTABLE_ERROR_STATUS
product: Windows
targetos: Windows
req.typenames: PCI_EXPRESS_CORRECTABLE_ERROR_STATUS, *PPCI_CORRECTABLE_ERROR_STATUS
---

# _PCI_EXPRESS_CORRECTABLE_ERROR_STATUS structure
The PCI_EXPRESS_CORRECTABLE_ERROR_STATUS structure describes a PCI Express (PCIe) correctable error status register of a PCIe advanced error reporting capability structure.

## Syntax
````
typedef union _PCI_EXPRESS_CORRECTABLE_ERROR_STATUS {
  struct {
    ULONG ReceiverError  :1;
    ULONG Reserved1  :5;
    ULONG BadTLP  :1;
    ULONG BadDLLP  :1;
    ULONG ReplayNumRollover  :1;
    ULONG Reserved2  :3;
    ULONG ReplayTimerTimeout  :1;
    ULONG AdvisoryNonFatalError  :1;
    ULONG Reserved3  :18;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_CORRECTABLE_ERROR_STATUS, *PPCI_CORRECTABLE_ERROR_STATUS;
````

## Members


`DUMMYSTRUCTNAME`



`AsULONG`

A ULONG representation of the contents of the PCI_EXPRESS_CORRECTABLE_ERROR_STATUS structure.

## Remarks
The PCI_EXPRESS_CORRECTABLE_ERROR_STATUS structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_CORRECTABLE_ERROR_STATUS structure is contained in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537457">PCI_EXPRESS_AER_CAPABILITY</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff537458">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a> structures.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | miniport.h (include Ntddk.h, Wdm.h, Miniport.h) |

## See Also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff537472">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537458">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537457">PCI_EXPRESS_AER_CAPABILITY</a>