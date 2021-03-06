---
UID: NS:d3d12umddi.D3D12DDI_SHADER_CAPS_0042
title: D3D12DDI_SHADER_CAPS_0042
author: windows-driver-content
description:
ms.assetid: eaa06c01-4aa1-4a27-abd1-68102a3f5d54
ms.author: windowsdriverdev
ms.date:
ms.topic: struct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.keywords: D3D12DDI_SHADER_CAPS_0042, D3D12DDI_SHADER_CAPS_0042,
req.header: d3d12umddi.h
req.include-header:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.ddi-compliance:
req.unicode-ansi:
req.max-support:
req.typenames: D3D12DDI_SHADER_CAPS_0042
topictype:
-	apiref
apitype:
-	HeaderDef
apilocation:
-	d3d12umddi.h
apiname:
-	D3D12DDI_SHADER_CAPS_0042
product: Windows
targetos: Windows
---

# D3D12DDI_SHADER_CAPS_0042 structure

## -description

The D3D12DDI_SHADER_CAPS_0042 structure contains display device shader capabilities that the driver supports.

## -struct-fields

### -field MinPrecision

Indicates a minimum precision of source and destination operands.

### -field DoubleOps

Double operations.

### -field ShaderSpecifiedStencilRef

The shader specified stencil reference.

### -field TypedUAVLoadAdditionalFormats

Typed Unordered Access View load additional formats.

### -field ROVs

Rasterizer ordered view.

### -field WaveOps

Wave operations.

### -field WaveLaneCountMin

The minimum wave lane count.

### -field WaveLaneCountMax

The maximum wave lane count.

### -field TotalLaneCount

The total lane count.

### -field Int64Ops

Native 64-bit operations.

### -field Native16BitOps

Native 16-bit operations.

