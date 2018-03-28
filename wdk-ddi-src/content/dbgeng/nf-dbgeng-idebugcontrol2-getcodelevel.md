---
UID: NF:dbgeng.IDebugControl2.GetCodeLevel
title: IDebugControl2::GetCodeLevel method
author: windows-driver-content
description: The GetCodeLevel method returns the current code level and is mainly used when stepping through code.
old-location: debugger\getcodelevel.htm
old-project: debugger
ms.assetid: 965565ee-ef4c-4a1d-a6f1-77b6d63c6ee8
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetCodeLevel method [Windows Debugging], GetCodeLevel method [Windows Debugging], IDebugControl interface, GetCodeLevel method [Windows Debugging], IDebugControl2 interface, GetCodeLevel method [Windows Debugging], IDebugControl3 interface, GetCodeLevel,IDebugControl2.GetCodeLevel, IDebugControl interface [Windows Debugging], GetCodeLevel method, IDebugControl2, IDebugControl2 interface [Windows Debugging], GetCodeLevel method, IDebugControl2::GetCodeLevel, IDebugControl3 interface [Windows Debugging], GetCodeLevel method, IDebugControl3::GetCodeLevel, IDebugControl::GetCodeLevel, IDebugControl_8533dd3f-f004-4d89-9f02-b7835fc6169e.xml, dbgeng/IDebugControl2::GetCodeLevel, dbgeng/IDebugControl3::GetCodeLevel, dbgeng/IDebugControl::GetCodeLevel, debugger.getcodelevel
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
-	IDebugControl.GetCodeLevel
-	IDebugControl2.GetCodeLevel
-	IDebugControl3.GetCodeLevel
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---


# GetCodeLevel method
The <b>GetCodeLevel</b> method returns the current code level and is mainly used when stepping through code.

## Syntax

````
HRESULT GetCodeLevel(
  [out] PULONG Level
);
````

## Parameters

`Level`

Receives the current code level.  <i>Level</i> can take one of the values in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
DEBUG_LEVEL_SOURCE

</td>
<td>
<i>Source mode</i>.  When stepping through code on the target, the size of a single step will be a line of source code.

</td>
</tr>
<tr>
<td>
DEBUG_LEVEL_ASSEMBLY

</td>
<td>
<i>Assembly mode</i>.  When stepping through code on the target, the size of a single step will be a single processor instruction.

</td>
</tr>
</table>


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
The method was successful.

</td>
</tr>
</table>

## Remarks

For more information about the code level, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560141">Using Source Files</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | dbgeng.h (include Dbgeng.h) |

## See Also

<a href="..\dbgeng\nn-dbgeng-idebugcontrol3.md">IDebugControl3</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol.md">IDebugControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556629">SetCodeLevel</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol2.md">IDebugControl2</a>