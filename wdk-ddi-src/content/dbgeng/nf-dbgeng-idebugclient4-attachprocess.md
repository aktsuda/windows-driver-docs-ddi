---
UID: NF:dbgeng.IDebugClient4.AttachProcess
title: IDebugClient4::AttachProcess method
author: windows-driver-content
description: The AttachProcess method connects the debugger engine to a user-modeprocess.
old-location: debugger\attachprocess.htm
old-project: debugger
ms.assetid: 0787da49-23e0-43e3-bb32-1221db32a449
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: AttachProcess method [Windows Debugging], AttachProcess method [Windows Debugging], IDebugClient interface, AttachProcess method [Windows Debugging], IDebugClient2 interface, AttachProcess method [Windows Debugging], IDebugClient3 interface, AttachProcess method [Windows Debugging], IDebugClient4 interface, AttachProcess method [Windows Debugging], IDebugClient5 interface, AttachProcess,IDebugClient4.AttachProcess, IDebugClient interface [Windows Debugging], AttachProcess method, IDebugClient2 interface [Windows Debugging], AttachProcess method, IDebugClient2::AttachProcess, IDebugClient3 interface [Windows Debugging], AttachProcess method, IDebugClient3::AttachProcess, IDebugClient4, IDebugClient4 interface [Windows Debugging], AttachProcess method, IDebugClient4::AttachProcess, IDebugClient5 interface [Windows Debugging], AttachProcess method, IDebugClient5::AttachProcess, IDebugClient::AttachProcess, IDebugClient_032236c1-3072-4226-919b-3f6f95635a20.xml, dbgeng/IDebugClient2::AttachProcess, dbgeng/IDebugClient3::AttachProcess, dbgeng/IDebugClient4::AttachProcess, dbgeng/IDebugClient5::AttachProcess, dbgeng/IDebugClient::AttachProcess, debugger.attachprocess
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
-	IDebugClient.AttachProcess
-	IDebugClient2.AttachProcess
-	IDebugClient3.AttachProcess
-	IDebugClient4.AttachProcess
-	IDebugClient5.AttachProcess
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---


# AttachProcess method
The <b>AttachProcess</b> method connects the <a href="https://msdn.microsoft.com/fa52a1f0-9397-48a5-acbd-ce5347c0baef">debugger engine</a> to a user-modeprocess.

## Syntax

````
HRESULT AttachProcess(
  [in] ULONG64 Server,
  [in] ULONG   ProcessId,
  [in] ULONG   AttachFlags
);
````

## Parameters

`Server`

Specifies the process server to use to attach to the process.  If <i>Server</i> is zero, the engine will connect to a local process without using a process server.

`ProcessId`

Specifies the process ID of the target process the debugger will attach to.

`AttachFlags`

Specifies the flags that control how the debugger attaches to the target process.  For details on these flags, see Remarks.


## Return Value

This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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

This method is available only for live user-mode debugging.

<div class="alert"><b>Note</b>    The engine doesn't completely attach to the process until the <a href="https://msdn.microsoft.com/library/windows/hardware/ff561229">WaitForEvent</a> method has been called.  Only after the process has generated an event -- for example, the create-process event -- does it become available in the debugger session.</div>
<div> </div>
For more information about creating and attaching to live user-mode targets, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552020">Live User-Mode Targets</a>.

The DEBUG_ATTACH_<i>XXX</i> bit-flags control how the <a href="https://msdn.microsoft.com/fa52a1f0-9397-48a5-acbd-ce5347c0baef">debugger engine</a> attaches to a user-mode process.  For the DEBUG_ATTACH_<i>XXX</i> options used when attaching to a kernel target, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538145">AttachKernel</a>.

The following table describes the possible flag values.



<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>
<b>DEBUG_ATTACH_NONINVASIVE</b>

</td>
<td>
Attach to the target noninvasively.  For more information about noninvasive debugging, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552274">Noninvasive Debugging (User Mode)</a>.

If this flag is set, then the flags DEBUG_ATTACH_EXISTING, DEBUG_ATTACH_INVASIVE_NO_INITIAL_BREAK, and DEBUG_ATTACH_INVASIVE_RESUME_PROCESS must not be set.

</td>
</tr>
<tr>
<td>
<b>DEBUG_ATTACH_EXISTING</b>

</td>
<td>
Re-attach to an application to which a debugger has already attached (and possibly abandoned).  For more information about re-attaching to targets, see <a href="https://msdn.microsoft.com/cc137185-58a7-44bf-b262-2698c46730f6">Re-attaching to the Target Application</a>.

If this flag is set, then the other DEBUG_ATTACH_<i>XXX</i> flags must not be set.

</td>
</tr>
<tr>
<td>
<b>DEBUG_ATTACH_NONINVASIVE_NO_SUSPEND</b>

</td>
<td>
Do not suspend the target's threads when attaching noninvasively.

If this flag is set, then the flag DEBUG_ATTACH_NONINVASIVE must also be set.

</td>
</tr>
<tr>
<td>
<b>DEBUG_ATTACH_INVASIVE_NO_INITIAL_BREAK</b>

</td>
<td>
(Windows XP and later)  Do not request an initial break-in when attaching to the target.

If this flag is set, then the flags DEBUG_ATTACH_NONINVASIVE and DEBUG_ATTACH_EXISTING must not be set.

</td>
</tr>
<tr>
<td>
<b>DEBUG_ATTACH_INVASIVE_RESUME_PROCESS</b>

</td>
<td>
If this flag is set, then the flags DEBUG_ATTACH_NONINVASIVE and DEBUG_ATTACH_EXISTING must not be set.

</td>
</tr>
</table>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | dbgeng.h (include Dbgeng.h) |

## See Also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff539237">ConnectProcessServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537786">AbandonCurrentProcess</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff558866">TerminateCurrentProcess</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540055">CreateProcessAndAttach2</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient.md">IDebugClient</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient2.md">IDebugClient2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539323">CreateProcess2</a>



<a href="https://msdn.microsoft.com/fa52a1f0-9397-48a5-acbd-ce5347c0baef">debugger engine</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548265">GetRunningProcessSystemIds</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient5.md">IDebugClient5</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient4.md">IDebugClient4</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient3.md">IDebugClient3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562135">.attach (Attach to Process)</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548243">GetRunningProcessDescription</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538145">AttachKernel</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541846">DetachCurrentProcess</a>