---
UID: NS:wudfwdm._PO_FX_COMPONENT_PERF_INFO
title: "_PO_FX_COMPONENT_PERF_INFO"
author: windows-driver-content
description: The PO_FX_COMPONENT_PERF_INFO structure describes all the sets of performance states for a single component within a device.
old-location: kernel\po_fx_component_perf_info.htm
old-project: kernel
ms.assetid: DA9C020F-18E7-4C6C-AEBB-81B099C80CD0
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: "*PPO_FX_COMPONENT_PERF_INFO, PO_FX_COMPONENT_PERF_INFO, PO_FX_COMPONENT_PERF_INFO structure [Kernel-Mode Driver Architecture], PPO_FX_COMPONENT_PERF_INFO, PPO_FX_COMPONENT_PERF_INFO structure pointer [Kernel-Mode Driver Architecture], _PO_FX_COMPONENT_PERF_INFO, kernel.po_fx_component_perf_info, wdm/PO_FX_COMPONENT_PERF_INFO, wdm/PPO_FX_COMPONENT_PERF_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wudfwdm.h
req.include-header: Wudfwdm.h
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
req.irql: Any level (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdm.h
api_name:
-	PO_FX_COMPONENT_PERF_INFO
product: Windows
targetos: Windows
req.typenames: PO_FX_COMPONENT_PERF_INFO, *PPO_FX_COMPONENT_PERF_INFO
req.product: Windows 10 or later.
---

# _PO_FX_COMPONENT_PERF_INFO structure
The <b>PO_FX_COMPONENT_PERF_INFO</b> structure describes  all the sets of performance states for a  single component within a device.

## Syntax
````
typedef struct _PO_FX_COMPONENT_PERF_INFO {
  ULONG                    PerfStateSetsCount;
  PO_FX_COMPONENT_PERF_SET PerfStateSets[ANYSIZE_ARRAY];
} PO_FX_COMPONENT_PERF_INFO, *PPO_FX_COMPONENT_PERF_INFO;
````

## Members


`PerfStateSetsCount`

The number of elements in the array <b>PerfStateSets</b> array.

`PerfStateSets`

This member is the first element in an array of one or more <a href="..\wudfwdm\ns-wudfwdm-_po_fx_component_perf_set.md">PO_FX_COMPONENT_PERF_SET</a> elements. Each  <b>PO_FX_COMPONENT_PERF_SET</b> represents one set of supported performance states for a component. If the array contains more than one element, the additional elements immediately follow the first element.

## Remarks
When a device driver calls the <a href="..\wdm\nf-wdm-pofxregistercomponentperfstates.md">PoFxRegisterComponentPerfStates</a> routine to register a component for performance state support with the power management framework (PoFx),  the driver can supply a <b>PO_FX_COMPONENT_PERF_INFO</b> structure that  describes the sets of the performance states supported by the component. The <b>PerfStateSets</b> member of the <b>PO_FX_COMPONENT_PERF_INFO</b> structure contains an array of <a href="..\wudfwdm\ns-wudfwdm-_po_fx_component_perf_set.md">PO_FX_COMPONENT_PERF_SET</a> structures that represent the supported performance states.

Most drivers are expected to define a single set of performance states per component. For example, a driver might define one set of performance states to control the clock frequency for a component. However, some drivers may need to define more than one performance state set to control multiple dimensions of performance states for a component. For example, a driver might define two sets of performance states to control the clock frequency and bus bandwidth.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows version** | Supported starting with Windows 10. Supported starting with Windows 10. |
| **Header** | wudfwdm.h (include Wudfwdm.h) |

## See Also

<a href="..\wdm\nf-wdm-pofxregistercomponentperfstates.md">PoFxRegisterComponentPerfStates</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn939352">Component-Level Performance State Management</a>



<a href="..\wudfwdm\ns-wudfwdm-_po_fx_component_perf_set.md">PO_FX_COMPONENT_PERF_SET</a>