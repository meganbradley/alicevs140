---
title: "CMFCAcceleratorKey::Format"
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
ms.assetid: 2ba5960a-7437-4e6d-9281-ef77cc74559d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAcceleratorKey::Format
Translates the ACCEL structure to its associated string value.  
  
## Syntax  
  
```  
void Format(  
   CString& str   
) const;  
```  
  
#### Parameters  
 [out] `str`  
 A reference to a `CString` object where the method writes the translated shortcut key.  
  
## Remarks  
 This method retrieves the string format of the associated shortcut key. You can set the string format of a [CMFCAcceleratorKey](../vs140/CMFCAcceleratorKey-Class.md) object using either the constructor or the method [CMFCAcceleratorKey::SetAccelerator](../vs140/CMFCAcceleratorKey--SetAccelerator.md).  
  
## Requirements  
 **Header:** afxacceleratorkey.h  
  
## See Also  
 [CMFCAcceleratorKey Class](../vs140/CMFCAcceleratorKey-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)