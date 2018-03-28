---
UID: NF:dbgeng.IDebugAdvanced2.GetSourceFileInformation
title: IDebugAdvanced2::GetSourceFileInformation method
author: windows-driver-content
description: The GetSourceFileInformation method returns specified information about a source file.
old-location: debugger\getsourcefileinformation.htm
old-project: debugger
ms.assetid: c854b3a7-963a-4386-b6fa-9c22b9d496a1
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetSourceFileInformation method [Windows Debugging], GetSourceFileInformation method [Windows Debugging], IDebugAdvanced2 interface, GetSourceFileInformation method [Windows Debugging], IDebugAdvanced3 interface, GetSourceFileInformation,IDebugAdvanced2.GetSourceFileInformation, IDebugAdvanced2, IDebugAdvanced2 interface [Windows Debugging], GetSourceFileInformation method, IDebugAdvanced2::GetSourceFileInformation, IDebugAdvanced3 interface [Windows Debugging], GetSourceFileInformation method, IDebugAdvanced3::GetSourceFileInformation, IDebugAdvanced_2f76d1fd-36fe-48c1-a131-eb4722d2af95.xml, dbgeng/IDebugAdvanced2::GetSourceFileInformation, dbgeng/IDebugAdvanced3::GetSourceFileInformation, debugger.getsourcefileinformation
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
-	IDebugAdvanced2.GetSourceFileInformation
-	IDebugAdvanced3.GetSourceFileInformation
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---


# GetSourceFileInformation method
The <b>GetSourceFileInformation</b> method returns specified information about a source file.

## Syntax

````
HRESULT GetSourceFileInformation(
  [in]            ULONG   Which,
  [in]            PSTR    SourceFile,
  [in]            ULONG64 Arg64,
  [in]            ULONG   Arg32,
  [out, optional] PVOID   Buffer,
  [in]            ULONG   BufferSize,
  [out, optional] PULONG  InfoSize
);
````

## Parameters

`Which`

Specifies the piece of information to return.  The <i>Which</i> parameter can take one of the values in the following table.





#### DEBUG_SRCFILE_SYMBOL_TOKEN

Returns a token representing the specified source file on a source server.  This token can be passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff545430">FindSourceFileAndToken</a> to retrieve information about the file. The token is returned to the <i>Buffer</i> buffer as an array of bytes.  The size of this token is a reflection of the size of the SrcSrv token. 



#### DEBUG_SRCFILE_SYMBOL_TOKEN_SOURCE_COMMAND_WIDE

Queries a source server for the command to extract the source file from source control.  This includes the name of the executable file and its command-line parameters. The command is returned to the <i>Buffer</i> buffer as a Unicode string.

`SourceFile`

Specifies the source file whose information is being requested.  The source file is looked up on all the source servers in the source path.

`Arg64`

Specifies a 64-bit argument.  The value of <i>Which</i> specifies the module whose symbol token is requested.  Regardless of the value of <i>Which</i>, <i>Arg64</i> is a location within the memory allocation of the module.

`Arg32`

Specifies a 32-bit argument.  This parameter is currently unused.

`Buffer`

Receives the requested symbol information.  The type of the data returned depends on the value of <i>Which</i>.  If <i>Buffer</i> is <b>NULL</b>, this information is not returned.

`BufferSize`

Specifies the size in bytes of the <i>Buffer</i> buffer. If <i>Buffer</i> is <b>NULL</b>, <i>BufferSize</i> must also be <b>NULL</b>.

`InfoSize`

Specifies the size in bytes of the information returned to the <i>Buffer</i> buffer.  This parameter can be <b>NULL</b> if the data is not required.


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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method was successful. However, the information would not fit in the <i>Buffer</i> buffer, so the information or name was truncated.

</td>
</tr>
</table>

## Remarks

For more information about source files, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560141">Using Source Files</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Desktop |
| **Header** | dbgeng.h (include Dbgeng.h) |

## See Also

<a href="..\dbgeng\nn-dbgeng-idebugadvanced2.md">IDebugAdvanced2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545430">FindSourceFileAndToken</a>



<a href="..\dbgeng\nn-dbgeng-idebugadvanced3.md">IDebugAdvanced3</a>