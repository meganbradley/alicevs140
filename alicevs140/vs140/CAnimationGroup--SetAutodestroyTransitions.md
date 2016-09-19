---
title: "CAnimationGroup::SetAutodestroyTransitions"
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
ms.assetid: 6d297c92-b2c3-41a7-b795-a55e01b3587a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationGroup::SetAutodestroyTransitions
Directs all animation objects that belong to group automatically destroy transitions.  
  
## Syntax  
  
```  
void SetAutodestroyTransitions(  
   BOOL bAutoDestroy = TRUE  
);  
```  
  
#### Parameters  
 `bAutoDestroy`  
 Specifies how to destroy transitions.  
  
## Remarks  
 Set this value to FALSE only if you allocate transitions on the stack. The default value is TRUE, therefore it's highly recommended to allocate transition objects using operator new.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationGroup Class](../vs140/CAnimationGroup-Class.md)