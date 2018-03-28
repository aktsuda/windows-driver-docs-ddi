---
UID: NF:dbgeng.IDebugControl2.GetDumpFormatFlags
title: IDebugControl2::GetDumpFormatFlags method
author: windows-driver-content
description: The GetDumpFormatFlags method returns the flags that describe what information is available in a dump file target.
old-location: debugger\getdumpformatflags.htm
old-project: debugger
ms.assetid: 86070c36-6702-42c8-b4fe-b3ef15ba418f
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetDumpFormatFlags method [Windows Debugging], GetDumpFormatFlags method [Windows Debugging], IDebugControl2 interface, GetDumpFormatFlags method [Windows Debugging], IDebugControl3 interface, GetDumpFormatFlags,IDebugControl2.GetDumpFormatFlags, IDebugControl2, IDebugControl2 interface [Windows Debugging], GetDumpFormatFlags method, IDebugControl2::GetDumpFormatFlags, IDebugControl3 interface [Windows Debugging], GetDumpFormatFlags method, IDebugControl3::GetDumpFormatFlags, IDebugControl_fc8bec39-ffc3-46bd-9d18-954f0420906f.xml, dbgeng/IDebugControl2::GetDumpFormatFlags, dbgeng/IDebugControl3::GetDumpFormatFlags, debugger.getdumpformatflags
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
-	IDebugControl2.GetDumpFormatFlags
-	IDebugControl3.GetDumpFormatFlags
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---


# GetDumpFormatFlags method
The <b>GetDumpFormatFlags</b> method returns the flags that describe what information is available in a dump file target.

## Syntax

````
HRESULT GetDumpFormatFlags(
  [out] PULONG FormatFlags
);
````

## Parameters

`FormatFlags`

Receives the flags that describe the information included in a dump file.  Different dump files support different sets of format information.  For example, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff541497">DEBUG_FORMAT_XXX</a> for a description of the flags used for user-mode Minidump files.


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

This method is only available when debugging crash dump files.  If the crash dump file is in a default format or does not have variable formats, zero will be returned to <i>FormatFlags</i>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | dbgeng.h (include Dbgeng.h) |

## See Also

<a href="..\dbgeng\nn-dbgeng-idebugcontrol3.md">IDebugControl3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561389">WriteDumpFileWide</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561382">WriteDumpFile2</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol2.md">IDebugControl2</a>