---
UID: NF:dbgeng.IDebugDataSpaces.WriteVirtual
title: IDebugDataSpaces::WriteVirtual method
author: windows-driver-content
description: The WriteVirtual method writes data to the target's virtual address space.
old-location: debugger\writevirtual.htm
old-project: debugger
ms.assetid: 52813320-90a4-4dca-9b9c-44aa22fc49de
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IDebugDataSpaces, IDebugDataSpaces interface [Windows Debugging], WriteVirtual method, IDebugDataSpaces2 interface [Windows Debugging], WriteVirtual method, IDebugDataSpaces2::WriteVirtual, IDebugDataSpaces3 interface [Windows Debugging], WriteVirtual method, IDebugDataSpaces3::WriteVirtual, IDebugDataSpaces4 interface [Windows Debugging], WriteVirtual method, IDebugDataSpaces4::WriteVirtual, IDebugDataSpaces::WriteVirtual, IDebugDataSpaces_2f8783ea-c7e4-438f-ad5b-898d0072a2f4.xml, WriteVirtual method [Windows Debugging], WriteVirtual method [Windows Debugging], IDebugDataSpaces interface, WriteVirtual method [Windows Debugging], IDebugDataSpaces2 interface, WriteVirtual method [Windows Debugging], IDebugDataSpaces3 interface, WriteVirtual method [Windows Debugging], IDebugDataSpaces4 interface, WriteVirtual,IDebugDataSpaces.WriteVirtual, dbgeng/IDebugDataSpaces2::WriteVirtual, dbgeng/IDebugDataSpaces3::WriteVirtual, dbgeng/IDebugDataSpaces4::WriteVirtual, dbgeng/IDebugDataSpaces::WriteVirtual, debugger.writevirtual
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dbgeng.h
api_name:
-	IDebugDataSpaces.WriteVirtual
-	IDebugDataSpaces2.WriteVirtual
-	IDebugDataSpaces3.WriteVirtual
-	IDebugDataSpaces4.WriteVirtual
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---


# WriteVirtual method
The <b>WriteVirtual</b> method writes data to the target's virtual address space.

## Syntax

````
HRESULT WriteVirtual(
  [in]            ULONG64 Offset,
  [in]            PVOID   Buffer,
  [in]            ULONG   BufferSize,
  [out, optional] PULONG  BytesWritten
);
````

## Parameters

`Offset`

Specifies the location in the target's virtual address space to be written.

`Buffer`

Specifies the buffer to write the memory from.

`BufferSize`

Specifies the size in bytes of the buffer.  This is also the number of bytes requested to be written.

`BytesWritten`

Receives the number of bytes that were written.  If it is set to <b>NULL</b>, this information is not returned.


## Return Value

This method can also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was at least partially successful.  <i>BytesWritten</i> indicates the number of bytes successfully written, which may be less than <i>BufferSize</i>.

</td>
</tr>
</table>

## Remarks

This method writes the buffer to the memory in the target's virtual address space.

This method may only write to a cache of memory data when storing data.  To avoid caching, use <a href="https://msdn.microsoft.com/library/windows/hardware/ff561473">WriteVirtualUncached</a> instead.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | dbgeng.h (include Dbgeng.h) |

## See Also

<a href="..\dbgeng\nn-dbgeng-idebugdataspaces2.md">IDebugDataSpaces2</a>



<a href="..\dbgeng\nn-dbgeng-idebugdataspaces4.md">IDebugDataSpaces4</a>



<a href="..\dbgeng\nn-dbgeng-idebugdataspaces3.md">IDebugDataSpaces3</a>



<a href="..\dbgeng\nn-dbgeng-idebugdataspaces.md">IDebugDataSpaces</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554359">ReadVirtual</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561473">WriteVirtualUncached</a>