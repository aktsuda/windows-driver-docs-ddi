---
UID: NF:dbgeng.IDebugClient4.CreateClient
title: IDebugClient4::CreateClient method
author: windows-driver-content
description: The CreateClient method creates a new client object for the current thread.
old-location: debugger\createclient.htm
old-project: debugger
ms.assetid: 61733b3e-87e9-4bb1-bed0-44efeffd7e4f
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CreateClient method [Windows Debugging], CreateClient method [Windows Debugging], IDebugClient interface, CreateClient method [Windows Debugging], IDebugClient2 interface, CreateClient method [Windows Debugging], IDebugClient3 interface, CreateClient method [Windows Debugging], IDebugClient4 interface, CreateClient method [Windows Debugging], IDebugClient5 interface, CreateClient,IDebugClient4.CreateClient, IDebugClient interface [Windows Debugging], CreateClient method, IDebugClient2 interface [Windows Debugging], CreateClient method, IDebugClient2::CreateClient, IDebugClient3 interface [Windows Debugging], CreateClient method, IDebugClient3::CreateClient, IDebugClient4, IDebugClient4 interface [Windows Debugging], CreateClient method, IDebugClient4::CreateClient, IDebugClient5 interface [Windows Debugging], CreateClient method, IDebugClient5::CreateClient, IDebugClient::CreateClient, IDebugClient_baa33ba0-bc95-4bfb-b8bf-b91598833599.xml, dbgeng/IDebugClient2::CreateClient, dbgeng/IDebugClient3::CreateClient, dbgeng/IDebugClient4::CreateClient, dbgeng/IDebugClient5::CreateClient, dbgeng/IDebugClient::CreateClient, debugger.createclient
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
-	IDebugClient.CreateClient
-	IDebugClient2.CreateClient
-	IDebugClient3.CreateClient
-	IDebugClient4.CreateClient
-	IDebugClient5.CreateClient
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---


# CreateClient method
The <b>CreateClient</b> method creates a new client object for the current thread.

## Syntax

````
HRESULT CreateClient(
  [out] IDebugClient **Client
);
````

## Parameters

`Client`

Receives an interface pointer for the new client.


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

This method creates a client that may be used in the current thread.

Clients are specific to the thread that created them.  Calls from other threads fail immediately.  The <b>CreateClient</b> method is a notable exception; it allows creation of a new client for a new thread. 

All callbacks for a client are made in the thread with which the client was created.

For more information about client objects and how they are used in the debugger engine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff539140">Client Objects</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | dbgeng.h (include Dbgeng.h) |

## See Also

<a href="..\dbgeng\nf-dbgeng-debugcreate.md">DebugCreate</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient5.md">IDebugClient5</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient4.md">IDebugClient4</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient3.md">IDebugClient3</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient.md">IDebugClient</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient2.md">IDebugClient2</a>