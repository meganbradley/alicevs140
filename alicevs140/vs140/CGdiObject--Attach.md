---
title: "CGdiObject::Attach"
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
ms.assetid: 44f7a4ab-4a3b-4f13-a0d8-3374b3674f6e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::Attach
Attaches a Windows GDI object to a `CGdiObject` object.  
  
## Syntax  
  
```  
  
      BOOL Attach(  
   HGDIOBJ hObject   
);  
```  
  
#### Parameters  
 `hObject`  
 A `HANDLE` to a Windows GDI object (for example, `HPEN` or `HBRUSH`).  
  
## Return Value  
 Nonzero if attachment is successful; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGdiObject::Detach](../vs140/CGdiObject--Detach.md)