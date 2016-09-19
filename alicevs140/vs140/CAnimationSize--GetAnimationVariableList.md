---
title: "CAnimationSize::GetAnimationVariableList"
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
ms.assetid: 47dc9fcc-3bd6-432a-95a6-8ae46296cbf9
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationSize::GetAnimationVariableList
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
 When the function returns, it contains pointers to two CAnimationVariable objects representing the width and height.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationSize Class](../vs140/CAnimationSize-Class.md)