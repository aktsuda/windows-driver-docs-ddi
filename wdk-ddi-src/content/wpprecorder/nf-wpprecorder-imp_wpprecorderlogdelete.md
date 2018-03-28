---
UID: NF:wpprecorder.imp_WppRecorderLogDelete
title: imp_WppRecorderLogDelete function
author: windows-driver-content
description: The WppRecorderLogDelete method deletes the specified recorder log.
old-location: devtest\wpprecorderlogdelete.htm
old-project: devtest
ms.assetid: AEE10756-7301-4B55-82A5-27CA595854EA
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: WppRecorderLogDelete, devtest.wpprecorderlogdelete, imp_WppRecorderLogDelete, imp_WppRecorderLogDelete function [Driver Development Tools], wpprecorder/imp_WppRecorderLogDelete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wpprecorder.h
req.include-header: 
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wpprecorder.h
api_name:
-	imp_WppRecorderLogDelete
product: Windows
targetos: Windows
req.typenames: WNODE_HEADER, *PWNODE_HEADER
req.product: Windows 10 or later.
---


# imp_WppRecorderLogDelete function
The <a href="..\wpprecorder\nf-wpprecorder-imp_wpprecorderlogdelete.md">WppRecorderLogDelete</a> method deletes the specified recorder log.

## Syntax

````
NTSTATUS imp_WppRecorderLogDelete(
   NULL RecorderLog
);
````

## Parameters

`WppCb`

TBD

`RecorderLog`

Handle to the recorder log to delete.


## Return Value

Returns STATUS_SUCCESS if completed successfully.

## Remarks

When a thread enters this function, no threads can subsequently  log to this buffer.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Target Platform** | Windows |
| **Header** | wpprecorder.h |