---
title: "CDC::CreateIC"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: ff5c8904-553a-4628-97b8-9fc3f5b07bf9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::CreateIC
Creates an information context for the specified device.  
  
## Syntax  
  
```  
  
      BOOL CreateIC(  
   LPCTSTR lpszDriverName,  
   LPCTSTR lpszDeviceName,  
   LPCTSTR lpszOutput,  
   const void* lpInitData   
);  
```  
  
#### Parameters  
 `lpszDriverName`  
 Points to a null-terminated string that specifies the filename (without extension) of the device driver (for example, "EPSON"). You can pass a `CString` object for this parameter.  
  
 `lpszDeviceName`  
 Points to a null-terminated string that specifies the name of the specific device to be supported (for example, "EPSON FX-80"). The `lpszDeviceName` parameter is used if the module supports more than one device. You can pass a `CString` object for this parameter.  
  
 `lpszOutput`  
 Points to a null-terminated string that specifies the file or device name for the physical output medium (file or port). You can pass a `CString` object for this parameter.  
  
 `lpInitData`  
 Points to device-specific initialization data for the device driver. The `lpInitData` parameter must be **NULL** if the device driver is to use the default initialization (if any) specified by the user through the Control Panel. See `CreateDC` for the data format for device-specific initialization.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The information context provides a fast way to get information about the device without creating a device context.  
  
 Device names follow these conventions: an ending colon (:) is recommended, but optional. Windows strips the terminating colon so that a device name ending with a colon is mapped to the same port as the same name without a colon. The driver and port names must not contain leading or trailing spaces. GDI output functions cannot be used with information contexts.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::CreateDC](../vs140/CDC--CreateDC.md)   
 [CreateIC](http://msdn.microsoft.com/library/windows/desktop/dd183505)   
 [CDC::DeleteDC](../vs140/CDC--DeleteDC.md)