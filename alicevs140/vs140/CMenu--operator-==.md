---
title: "CMenu::operator =="
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
ms.assetid: 376bc3e1-d92f-40a1-a9b1-a886500914b6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::operator ==
Determines if two menus are logically equal.  
  
## Syntax  
  
```  
  
      BOOL operator==(   
   const CMenu& menu   
) const;  
```  
  
#### Parameters  
 `menu`  
 A `CMenu` object for comparison.  
  
## Remarks  
 Tests if a menu object on the left side is equal (in terms of the `HMENU` value) to a menu object on the right side.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)