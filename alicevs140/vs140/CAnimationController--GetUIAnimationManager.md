---
title: "CAnimationController::GetUIAnimationManager"
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
ms.assetid: 9d05bd0b-e2ea-471c-ae91-ac1652e298fa
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::GetUIAnimationManager
Provides access to encapsulated IUIAnimationManager object.  
  
## Syntax  
  
```  
IUIAnimationManager* GetUIAnimationManager();  
```  
  
## Return Value  
 A pointer to IUIAnimationManager interface or NULL, if creation of animation manager failed.  
  
## Remarks  
 If current OS does not support Windows Animation API, this method returns NULL and after that all subsequent calls on CAnimationController::IsValid return FALSE. You may need to access IUIAnimationManager in order to call its interface methods, which are not wrapped by animation controller.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)