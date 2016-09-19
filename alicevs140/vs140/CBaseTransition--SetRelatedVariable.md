---
title: "CBaseTransition::SetRelatedVariable"
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
ms.assetid: 088c8d6d-64dd-49d0-bdb0-09720c428007
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTransition::SetRelatedVariable
Establishes a relationship between animation variable and transition.  
  
## Syntax  
  
```  
void SetRelatedVariable(  
   CAnimationVariable* pVariable  
);  
```  
  
#### Parameters  
 `pVariable`  
 A pointer to related animation variable.  
  
## Remarks  
 Establishes a relationship between animation variable and transition. A transition can be applied only to one variable.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseTransition Class](../vs140/CBaseTransition-Class.md)