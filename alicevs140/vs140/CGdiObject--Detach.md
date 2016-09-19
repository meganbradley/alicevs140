---
title: "CGdiObject::Detach"
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
ms.assetid: 6adee743-ab16-46e1-9719-5c65de8de11b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::Detach
Detaches a Windows GDI object from a `CGdiObject` object and returns a handle to the Windows GDI object.  
  
## Syntax  
  
```  
  
HGDIOBJ Detach( );  
```  
  
## Return Value  
 A `HANDLE` to the Windows GDI object detached; otherwise **NULL** if no GDI object is attached.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGdiObject::Attach](../vs140/CGdiObject--Attach.md)