---
UID: NF:dbgeng.IDebugControl5.GetBreakpointByGuid
title: IDebugControl5::GetBreakpointByGuid
author: windows-driver-content
description: The GetBreakpointByGuid method returns the breakpoint with the specified breakpoint GUID.
old-location: debugger\idebugcontrol5_getbreakpointbyguid.htm
old-project: debugger
ms.assetid: AC316591-CCF9-4040-B1A3-29AB2033B673
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetBreakpointByGuid, GetBreakpointByGuid method [Windows Debugging], GetBreakpointByGuid method [Windows Debugging],IDebugControl5 interface, IDebugControl5 interface [Windows Debugging],GetBreakpointByGuid method, IDebugControl5.GetBreakpointByGuid, IDebugControl5::GetBreakpointByGuid, dbgeng/IDebugControl5::GetBreakpointByGuid, debugger.idebugcontrol5_getbreakpointbyguid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: 
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
-	IDebugControl5.GetBreakpointByGuid
product:
- Windows
targetos: Windows
req.typenames: 
---

# IDebugControl5::GetBreakpointByGuid


## -description


The GetBreakpointByGuid method returns the breakpoint with the specified breakpoint GUID.


## -parameters




### -param Guid [in]

Specifies the breakpoint GUID of the breakpoint to return.


### -param Bp [out]

Receives the breakpoint.


## -returns



This method can also return other error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
No breakpoint was found with the given GUID, or the breakpoint with the specified GUID does not belong to the current process, or the breakpoint with the given GUID is private (see <a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>). 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539284">Controlling Breakpoint Flags and Parameters</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn818562">IDebugControl5</a>
 

 

