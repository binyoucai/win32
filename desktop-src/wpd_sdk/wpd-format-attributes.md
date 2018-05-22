---
Description: 'For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service. These attributes are returned by the IPortableDeviceServiceCapabilities::GetFormatAttributes method.'
ms.assetid: '53282e01-54da-4adf-8a09-2086d6398275'
title: Format Attributes
---

# Format Attributes

For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service. These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](iportabledeviceservicecapabilities-getformatattributes.md) method.

## 



| **Attribute**                        | **VarType**    | **Description**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **WPD\_FORMAT\_ATTRIBUTE\_MIMETYPE** | **VT\_LPWSTR** | The format MIME type.                                                                                                     |
| **WPD\_FORMAT\_ATTRIBUTE\_NAME**     | **VT\_LPWSTR** | A string that specifies the script-friendly name of the format. Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'. |



�

## Requirements



|                   |                                                                                             |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## See also

<dl> <dt>

[**Properties and Attributes**](properties-and-attributes.md)
</dt> </dl>

�

�



