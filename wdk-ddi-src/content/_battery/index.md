---
UID: TP:battery
author: windows-driver-content
ms.assetid: 7433fa8b-bcff-3cc7-a61e-27c29a2f632b
ms.author: windowsdriverdev
ms.date: 05/09/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Battery

## -description

Overview of the Battery technology.

To develop Battery, you need these headers:

 * [charging.h](..\charging\index.md)
 * [hpmi.h](..\hpmi\index.md)
 * [upssvc.h](..\upssvc\index.md)

For the programming guide, see [Battery](https://docs.microsoft.com/en-us/windows-hardware/drivers/battery).

## Functions

| Title   | Description   |
| ---- |:---- |
| [UPSCancelWait function](..\upssvc\nf-upssvc-upscancelwait.md) | The UPSCancelWait function cancels all waits initiated by calls to UPSWaitForStateChange. |
| [UPSGetState function](..\upssvc\nf-upssvc-upsgetstate.md) | The UPSGetState function returns the operational state of the UPS. |
| [UPSInit function](..\upssvc\nf-upssvc-upsinit.md) | The UPSInit function initializes a UPS minidriver, opens communication to the UPS unit, updates the registry, and causes the minidriver to start monitoring the UPS unit. |
| [UPSStop function](..\upssvc\nf-upssvc-upsstop.md) | The UPSStop function causes a UPS minidriver to stop monitoring its UPS unit. |
| [UPSTurnOff function](..\upssvc\nf-upssvc-upsturnoff.md) | The UPSTurnOff function turns off the UPS unit's power outlets, after a specified delay time. |
| [UPSWaitForStateChange function](..\upssvc\nf-upssvc-upswaitforstatechange.md) | The UPSWaitForStateChange function waits until a specified UPS state changes, or until a time-out interval elapses. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_BATTERYPROVISIONINGSTATUS structure](..\charging\ns-charging-_batteryprovisioningstatus.md) | This structure is for internal use only. |
| [_CAD_POWER_SOURCE_INFO structure](..\charging\ns-charging-_cad_power_source_info.md) | This structure is for internal use only. |
| [_CAD_POWER_SOURCE_INFO_USB structure](..\charging\ns-charging-_cad_power_source_info_usb.md) | This structure is for internal use only. |
| [_CHARGINGSTATUSCOMPLETE structure](..\charging\ns-charging-_chargingstatuscomplete.md) | This structure is for internal use only. |
| [_CONFIGURABLE_CHARGER_PROPERTY_HEADER structure](..\charging\ns-charging-_configurable_charger_property_header.md) | The CONFIGURABLE_CHARGER_PROPERTY_HEADER structure is a header that is used to create your own structure as an input to IOCTL_INTERNAL_CONFIGURE_CHARGER_PROPERTY. |
| [_POWERSOURCESTATUS structure](..\charging\ns-charging-_powersourcestatus.md) | This struct is for internal use only. |
| [_POWERSOURCEUPDATE structure](..\charging\ns-charging-_powersourceupdate.md) | This structure is for internal use only. |
| [_POWERSOURCEUPDATEEX structure](..\charging\ns-charging-_powersourceupdateex.md) | This structure is for internal use only. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_POWERSOURCEID enumeration](..\charging\ne-charging-_powersourceid.md) | This enum is for internal use only. |

## I/O control codes

| Title   | Description   |
| ---- |:---- |
| [IOCTL_CAD_DISABLE_CHARGING IOCTL](..\charging\ni-charging-ioctl_cad_disable_charging.md) | This IOCTL is for internal use only. |
| [IOCTL_CAD_GET_BATTERY_PROVISIONING_STATUS IOCTL](..\charging\ni-charging-ioctl_cad_get_battery_provisioning_status.md) | This IOCTL is for internal use only. |
| [IOCTL_CAD_GET_CHARGING_STATUS_COMPLETE IOCTL](..\charging\ni-charging-ioctl_cad_get_charging_status_complete.md) | This IOCTL is for internal use only. |
| [IOCTL_CAD_POWER_SOURCE_UPDATE_EX IOCTL](..\charging\ni-charging-ioctl_cad_power_source_update_ex.md) | This IOCTL is for internal use only. |
| [IOCTL_INTERNAL_CAD_POWER_SOURCE_UPDATE IOCTL](..\charging\ni-charging-ioctl_internal_cad_power_source_update.md) | This IOCTL is for internal use only. |
| [IOCTL_INTERNAL_CONFIGURE_CHARGER_PROPERTY IOCTL](..\charging\ni-charging-ioctl_internal_configure_charger_property.md) | The IOCTL_INTERNAL_CONFIGURE_CHARGER_PROPERTY control code is sent from a configurable charger to a device that handles configurable chargers. It configures charger properties. |
