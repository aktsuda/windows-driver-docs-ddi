---
UID: NI:pointofservicedriverinterface.IOCTL_POINT_OF_SERVICE_RETRIEVE_STATISTICS
title: IOCTL_POINT_OF_SERVICE_RETRIEVE_STATISTICS
author: windows-driver-content
description: This I/O control function returns unified point of service (UPOS) standard information about a device such as its category, manufacturer, and firmware revision number.
old-location: pos\ioctl_point_of_service_retrieve_statistics.htm
old-project: pos
ms.assetid: 8c63ef41-e4dd-4b34-a897-c9bec13f4211
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: _PosPropertyId, PosPropertyId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: pointofservicedriverinterface.h
req.include-header: Pointofservicedriverinterface.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IOCTL_POINT_OF_SERVICE_RETRIEVE_STATISTICS
req.alt-loc: pointofservicedriverinterface.h
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
req.typenames: PosPropertyId
---

# IOCTL_POINT_OF_SERVICE_RETRIEVE_STATISTICS IOCTL



## -description
This I/O control function returns unified point of service (UPOS) standard information about a device such as its category, manufacturer, and firmware revision number.



## -ioctlparameters

### -input-buffer
[in] Not used with this operation; set to <b>NULL</b>.


### -input-buffer-length
Not used with this operation; set to <b>0</b> (zero).


### -output-buffer
Pointer to the <a href="..\pointofservicedriverinterface\ns-pointofservicedriverinterface-_posstatisticsheader.md">PosStatisticsHeader</a> structure that contains the statistics.


### -output-buffer-length
Size of the output buffer in bytes. Set to sizeof(<i>PosStatisticsHeader</i>).


### -in-out-buffer

<text></text>

### -inout-buffer-length

<text></text>

### -status-block
I/O Status block
Returns <b>TRUE</b> if successful; otherwise, returns <b>FALSE</b>.

To get extended error information, call <a href="http://go.microsoft.com/fwlink/p/?LinkId=316871">GetLastError</a>. The following list shows common error values:



Statistic reporting is not supported.

The output buffer is not large enough to hold the statistics.


## -remarks