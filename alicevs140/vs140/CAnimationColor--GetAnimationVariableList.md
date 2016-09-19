---
title: "CAnimationColor::GetAnimationVariableList"
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
ms.assetid: 0a3453f3-04bf-40cf-a3cd-351008cdc017
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationColor::GetAnimationVariableList
Puts the encapsulated animation variables into a list.  
  
## Syntax  
  
```  
virtual void GetAnimationVariableList(  
   CList<CAnimationVariable*,  
   CAnimationVariable*>& lst  
);  
```  
  
#### Parameters  
 `lst`  
 When the function returns, it contains pointers to three CAnimationVariable objects representing red, green and blue components.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationColor Class](../vs140/CAnimationColor-Class.md)