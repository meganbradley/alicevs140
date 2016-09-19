---
title: "CGdiObject::operator !="
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
ms.assetid: 45aa8156-03a7-49ed-bc9c-2b85fb1d9623
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::operator !=
Determines if two GDI objects are logically not equal.  
  
## Syntax  
  
```  
  
      BOOL operator!=(  
   const CGdiObject& obj  
) const;  
```  
  
#### Parameters  
 `obj`  
 A pointer to an existing `CGdiObject`.  
  
## Remarks  
 Determines if a GDI object on the left side is not equal to a GDI object on the right side.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGdiObject::operator ==](../vs140/CGdiObject--operator-==.md)