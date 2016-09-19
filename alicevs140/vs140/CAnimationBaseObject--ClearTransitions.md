---
title: "CAnimationBaseObject::ClearTransitions"
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
ms.assetid: 70d27bfc-f499-4d88-90c2-6eae08a3be56
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::ClearTransitions
Removes all related transitions.  
  
## Syntax  
  
```  
virtual void ClearTransitions(  
   BOOL bAutodestroy  
);  
```  
  
#### Parameters  
 `bAutodestroy`  
 Specifies whether to destroy transition objects automatically, or just remove them from the related list.  
  
## Remarks  
 Removes all related transitions and destroys them if bAutodestroy or m_bAutodestroyTransitions flag is TRUE. Transitions should be destroyed automatically only if they are not allocated on the stack. If the above flags are FALSE, transitions are just removed from the internal list of related transitions.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)