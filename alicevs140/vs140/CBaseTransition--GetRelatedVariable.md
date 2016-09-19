---
title: "CBaseTransition::GetRelatedVariable"
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
ms.assetid: bfa97168-8edc-4401-b70a-a13f25e89320
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTransition::GetRelatedVariable
Returns a pointer to related variable.  
  
## Syntax  
  
```  
CAnimationVariable* GetRelatedVariable();  
```  
  
## Return Value  
 A valid pointer to animation variable, or NULL if an animation variable has not been set by SetRelatedVariable.  
  
## Remarks  
 This is an accessor to related animation variable.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseTransition Class](../vs140/CBaseTransition-Class.md)