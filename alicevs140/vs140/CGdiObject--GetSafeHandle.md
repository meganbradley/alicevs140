---
title: "CGdiObject::GetSafeHandle"
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
ms.assetid: 70442824-fdf1-435b-85c1-f28db7784559
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::GetSafeHandle
Returns `m_hObject` unless **this** is **NULL**, in which case **NULL** is returned.  
  
## Syntax  
  
```  
  
HGDIOBJ GetSafeHandle( ) const;  
```  
  
## Return Value  
 A `HANDLE` to the attached Windows GDI object; otherwise **NULL** if no object is attached.  
  
## Remarks  
 This is part of the general handle interface paradigm and is useful when **NULL** is a valid or special value for a handle.  
  
## Example  
 See the example for [CWnd::IsWindowEnabled](../vs140/CWnd--IsWindowEnabled.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)