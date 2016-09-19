---
title: "CBaseTransition::GetType"
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
ms.assetid: 82e86c05-1fe1-42d5-a242-4e501704b83e
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTransition::GetType
Returns transition type.  
  
## Syntax  
  
```  
TRANSITION_TYPE GetType() const;  
```  
  
## Return Value  
 One of TRANSITION_TYPE enumerated values.  
  
## Remarks  
 This method can be used to identify a transition object by its type. The type is set in a constructor in a derived class.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseTransition Class](../vs140/CBaseTransition-Class.md)