---
title: "CAnimationBaseObject::CreateTransitions"
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
ms.assetid: afd5fbf9-309e-46bd-80f8-f5b000b5ed3f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::CreateTransitions
Creates transitions associated with an animation object.  
  
## Syntax  
  
```  
BOOL CreateTransitions();  
```  
  
## Return Value  
 TRUE if transitions were created successfully; otherwise FALSE.  
  
## Remarks  
 Loops over list of animation variables encapsulated in a derived animation object and creates transitions associated with each animation variable.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)