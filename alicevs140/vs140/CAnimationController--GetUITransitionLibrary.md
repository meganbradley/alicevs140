---
title: "CAnimationController::GetUITransitionLibrary"
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
ms.assetid: 19ee177d-b3e7-43ba-9597-8087c939bea4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::GetUITransitionLibrary
Provides access to encapsulated IUIAnimationTransitionLibrary object.  
  
## Syntax  
  
```  
IUIAnimationTransitionLibrary* GetUITransitionLibrary();  
```  
  
## Return Value  
 A pointer to IUIAnimationTransitionLibrary interface or NULL, if creation of transition library failed.  
  
## Remarks  
 If current OS does not support Windows Animation API, this method returns NULL and after that all subsequent calls on CAnimationController::IsValid return FALSE.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)