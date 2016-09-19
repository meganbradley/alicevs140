---
title: "CAnimationBaseObject::GetAutodestroyTransitions"
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
ms.assetid: 7fc33559-0341-4391-812e-c68c7f80f2a4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationBaseObject::GetAutodestroyTransitions
Tells whether related transition are destroyed automatically.  
  
## Syntax  
  
```  
BOOL GetAutodestroyTransitions() const;  
```  
  
## Return Value  
 If TRUE, related transitions are destroyed automatically; if FALSE, transition objects should be deallocated by calling application.  
  
## Remarks  
 By default this flag is TRUE. Set this flag only if you allocated transition on the stack and/or transitions should be deallocated by the calling application.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationBaseObject Class](../vs140/CAnimationBaseObject-Class.md)