---
UID: NS:miniport._CM_MCA_POS_DATA
title: "_CM_MCA_POS_DATA"
author: windows-driver-content
description: The CM_MCA_POS_DATA structure is obsolete. It defines IBM-compatible MCA POS configuration information for a slot.
old-location: kernel\cm_mca_pos_data.htm
old-project: kernel
ms.assetid: 2b14eef2-dac4-48c8-b2a2-96bf085171aa
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: "*PCM_MCA_POS_DATA, CM_MCA_POS_DATA, CM_MCA_POS_DATA structure [Kernel-Mode Driver Architecture], PCM_MCA_POS_DATA, PCM_MCA_POS_DATA structure pointer [Kernel-Mode Driver Architecture], _CM_MCA_POS_DATA, kernel.cm_mca_pos_data, kstruct_a_a0edcef2-abf9-4660-8f40-76a2f8ff1193.xml, wdm/CM_MCA_POS_DATA, wdm/PCM_MCA_POS_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: miniport.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
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
-	Wdm.h
api_name:
-	CM_MCA_POS_DATA
product: Windows
targetos: Windows
req.typenames: CM_MCA_POS_DATA, *PCM_MCA_POS_DATA
---

# _CM_MCA_POS_DATA structure
The <b>CM_MCA_POS_DATA</b> structure is <u>obsolete</u>. It defines IBM-compatible MCA POS configuration information for a slot.

## Syntax
````
typedef struct _CM_MCA_POS_DATA {
  USHORT AdapterId;
  UCHAR  PosData1;
  UCHAR  PosData2;
  UCHAR  PosData3;
  UCHAR  PosData4;
} CM_MCA_POS_DATA, *PCM_MCA_POS_DATA;
````

## Members


`AdapterId`



`PosData1`



`PosData2`



`PosData3`



`PosData4`



## Remarks
This structure is used by the obsolete <a href="https://msdn.microsoft.com/library/windows/hardware/ff546599">HalGetBusData</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff546606">HalGetBusDataByOffset</a> routines.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | miniport.h (include Wdm.h, Ntddk.h, Ntifs.h, Miniport.h) |

## See Also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff546599">HalGetBusData</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546606">HalGetBusDataByOffset</a>