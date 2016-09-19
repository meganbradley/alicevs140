---
title: "CGdiObject::operator =="
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
ms.assetid: 7b89e15d-3548-4b0c-89ed-6f701912b84e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::operator ==
Determines if two GDI objects are logically equal.  
  
## Syntax  
  
```  
  
      BOOL operator==(  
   const CGdiObject& obj  
) const;  
```  
  
#### Parameters  
 `obj`  
 A reference to an existing `CGdiObject`.  
  
## Remarks  
 Determines if a GDI object on the left side is equal to a GDI object on the right side.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGdiObject::operator !=](../vs140/CGdiObject--operator-!=.md)