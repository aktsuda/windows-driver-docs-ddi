---
UID: NF:dbgeng.IDebugRegisters.GetFrameOffset
title: IDebugRegisters::GetFrameOffset method
author: windows-driver-content
description: The GetFrameOffset method returns the location of the stack frame for the current function.
old-location: debugger\getframeoffset.htm
old-project: debugger
ms.assetid: 09473106-3ab8-43ee-a424-2930b6bd3fcf
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetFrameOffset method [Windows Debugging], GetFrameOffset method [Windows Debugging], IDebugRegisters interface, GetFrameOffset method [Windows Debugging], IDebugRegisters2 interface, GetFrameOffset,IDebugRegisters.GetFrameOffset, IDebugRegisters, IDebugRegisters interface [Windows Debugging], GetFrameOffset method, IDebugRegisters2 interface [Windows Debugging], GetFrameOffset method, IDebugRegisters2::GetFrameOffset, IDebugRegisters::GetFrameOffset, IDebugRegisters_c3f31f5b-76d4-4910-b1a1-f3050c20e815.xml, dbgeng/IDebugRegisters2::GetFrameOffset, dbgeng/IDebugRegisters::GetFrameOffset, debugger.getframeoffset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: DbgEng.h
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
-	IDebugRegisters.GetFrameOffset
-	IDebugRegisters2.GetFrameOffset
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---


# GetFrameOffset method
The <b>GetFrameOffset</b> method returns the location of the stack frame for the current function.

## Syntax

````
HRESULT GetFrameOffset(
  [out] PULONG64 Offset
);
````

## Parameters

`Offset`

The location in the target's virtual address space of the stack frame for the current function.


## Return Value

This list does not contain all the errors that might occur.  For a list of possible errors, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff549771">HRESULT Values</a>.

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
The method was successful.

</td>
</tr>
</table>

## Remarks

The meaning of value returned by this method is architecture-specific.

The method <a href="https://msdn.microsoft.com/library/windows/hardware/ff546815">GetFrameOffset2</a> performs the same task as this method but also allows the register source to be specified.

For an overview of the <a href="..\dbgeng\nn-dbgeng-idebugregisters.md">IDebugRegisters</a> interface and other register-related methods, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff554369">Registers</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | dbgeng.h (include DbgEng.h) |

## See Also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff546815">GetFrameOffset2</a>



<a href="..\dbgeng\nn-dbgeng-idebugregisters.md">IDebugRegisters</a>



<a href="..\dbgeng\nn-dbgeng-idebugregisters2.md">IDebugRegisters2</a>