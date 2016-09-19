---
title: "CAnimationVariable::GetParentAnimationObject"
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
ms.assetid: 3e93588b-9bb9-457f-afff-99ab0f1a5c89
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationVariable::GetParentAnimationObject
Returns the parent animation object.  
  
## Syntax  
  
```  
CAnimationBaseObject* GetParentAnimationObject();  
```  
  
## Return Value  
 A pointer to parent animation object, if relationship was established, otherwise NULL.  
  
## Remarks  
 This method can be called to retrieve a pointer to a parent animation object (a container).  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationVariable Class](../vs140/CAnimationVariable-Class.md)