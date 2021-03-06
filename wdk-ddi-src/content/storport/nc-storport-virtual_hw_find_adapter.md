---
UID: NC:storport.VIRTUAL_HW_FIND_ADAPTER
title: VIRTUAL_HW_FIND_ADAPTER
author: windows-driver-content
description: The Storport virtual miniport uses configuration information supplied to the VirtualHwStorFindAdapter routine to further initialize itself.
old-location: storage\virtualhwstorfindadapter.htm
old-project: storage
ms.assetid: 55c16545-194e-4d23-b2e6-26821180eafa
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: VIRTUAL_HW_FIND_ADAPTER, VirtualHwStorFindAdapter, VirtualHwStorFindAdapter routine [Storage Devices], storage.virtualhwstorfindadapter, storport/VirtualHwStorFindAdapter, storvmini_d41a0c2e-d224-4cfd-95e1-997b6a54904b.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
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
-	UserDefined
api_location:
-	Storport.h
api_name:
-	VirtualHwStorFindAdapter
product:
- Windows
targetos: Windows
req.typenames: 
---

# VIRTUAL_HW_FIND_ADAPTER callback function


## -description


The Storport virtual miniport uses configuration information supplied to the <b>VirtualHwStorFindAdapter</b> routine to further initialize itself.


## -parameters




### -param DeviceExtension

A pointer to the miniport driver's per-adapter non-paged storage area. The operating system-specific port driver allocates memory for and initializes this extension with zeros before it calls the miniport's <b>VirtualHwStorFindAdapter</b> routine.


### -param HwContext

A pointer to the PDO in the device stack. The HBA itself is the FDO. The PDO might belong to the Pci.sys driver if the miniport driver controls physical hardware. But in the case of a virtual miniport driver, the PDO belongs to the PnP manager.


### -param BusInformation

A pointer to the miniport's functional device object  (FDO).


### -param LowerDevice

A pointer to the device object controlled by the miniport's FDO.


### -param ArgumentString

A pointer to a null-terminated ASCII string. This string, if supplied, contains device information from the registry such as a base parameter.


### -param ConfigInfo

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff567785">PORT_CONFIGURATION_INFORMATION</a> structure. The port driver initializes this structure with any known configuration information, such as values that the miniport driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff552644">DriverEntry</a> set in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568010">VIRTUAL_HW_INITIALIZATION_DATA</a>. <b>VirtualHwStorFindAdapter</b>  must use any supplied information to determine if the virtual HBA it describes is one that the miniport driver supports. If so, <b>VirtualHwStorFindAdapter</b> initializes and configures that HBA and fills in any missing configuration information. If possible, a miniport driver should have default configuration values for each type of HBA that it supports, in the event that the operating system-dependent port driver cannot supply additional configuration information that was not provided by the miniport driver's <b>DriverEntry</b> routine.


### -param Again

Not used.


## -returns



<b>VirtualHwStorFindAdapter</b> must return one of the following status values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SP_RETURN_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a supported HBA was found and that the HBA-relevant configuration information was determined successfully and set in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567785">PORT_CONFIGURATION_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SP_RETURN_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Indicates that an HBA was found, but an error occurred when it obtained the configuration information. If possible, such an error should be logged with <a href="https://msdn.microsoft.com/library/windows/hardware/ff564652">ScsiPortLogError</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SP_RETURN_BAD_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the supplied configuration information was invalid for the adapter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SP_RETURN_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that no supported HBA was found for the supplied configuration information.

</td>
</tr>
</table>
 




## -remarks



The <b>VirtualDevice</b> field in the configuration information structure must be set to <b>TRUE</b>. Other fields can be set as needed.

The port driver calls the Storport virtual miniport's <b>VirtualHwStorFindAdapter</b> at PASSIVE_LEVEL.

The name <b>VirtualHwStorFindAdapter</b> is placeholder text for the actual routine name. The actual prototype of this routine is defined in Srb.h as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef
ULONG
VIRTUAL_HW_FIND_ADAPTER (
  _In_ PVOID  DeviceExtension,
  _In_ PVOID  HwContext,
  _In_ PVOID  BusInformation,
  _In_ PVOID  LowerDevice,
  _In_ PCHAR  ArgumentString,
  _Inout_ PPORT_CONFIGURATION_INFORMATION  ConfigInfo,
  _Out_ PBOOLEAN Again
  );</pre>
</td>
</tr>
</table></span></div>

#### Examples

To define an <b>VirtualHwStorFindAdapter</b> callback function, you must first provide a function declaration that identifies the type of callback function you’re defining. Windows provides a set of callback function types for drivers. Declaring a function using the callback function types helps <a href="https://msdn.microsoft.com/2F3549EF-B50F-455A-BDC7-1F67782B8DCA">Code Analysis for Drivers</a>, <a href="https://msdn.microsoft.com/74feeb16-387c-4796-987a-aff3fb79b556">Static Driver Verifier</a> (SDV), and other verification tools find errors, and it’s a requirement for writing drivers for the Windows operating system.

 For example, to define a <b>VirtualHwStorFindAdapter</b> callback routine that is named <i>MyVirtualHwFindAdapter</i>, use the <b>VIRTUAL_HW_FIND_ADAPTER</b> type as shown in this code example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>VIRTUAL_HW_FIND_ADAPTER MyVirtualHwFindAdapter;</pre>
</td>
</tr>
</table></span></div>
Then, implement your callback routine as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>_Use_decl_annotations_
ULONG
MyVirtualHwFindAdapter (
  _In_ PVOID  DeviceExtension,
  _In_ PVOID  HwContext,
  _In_ PVOID  BusInformation,
  _In_ PVOID  LowerDevice,
  _In_ PCHAR  ArgumentString,
  _Inout_ PPORT_CONFIGURATION_INFORMATION  ConfigInfo,
  _Out_ PBOOLEAN Again
  );
  {
      ...
  }</pre>
</td>
</tr>
</table></span></div>
The <b>VIRTUAL_HW_FIND_ADAPTER</b> function type is defined in the Storport.h header file. To more accurately identify errors when you run the code analysis tools, be sure to add the _Use_decl_annotations_ annotation to your function definition. The _Use_decl_annotations_ annotation ensures that the annotations that are applied to the <b>VIRTUAL_HW_FIND_ADAPTER</b> function type in the header file are used. For more information about the requirements for function declarations, see <a href="https://msdn.microsoft.com/40BD11CD-A559-4F90-BF39-4ED2FB800392">Declaring Functions Using Function Role Types for Storport Drivers</a>. For information about _Use_decl_annotations_, see <a href="https://msdn.microsoft.com/en-us/library/jj159529.aspx">Annotating Function Behavior</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557390">HwStorFindAdapter</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567785">PORT_CONFIGURATION_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564652">ScsiPortLogError</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568010">VIRTUAL_HW_INITIALIZATION_DATA</a>
 

 

