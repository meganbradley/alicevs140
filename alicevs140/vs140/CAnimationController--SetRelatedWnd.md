---
title: "CAnimationController::SetRelatedWnd"
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
ms.assetid: 021e9cb1-1cfa-4ee5-ba94-cd3cf33c4b85
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationController::SetRelatedWnd
Establishes a relationship between animation controller and a window.  
  
## Syntax  
  
```  
void SetRelatedWnd(  
   CWnd* pWnd  
);  
```  
  
#### Parameters  
 `pWnd`  
 A pointer to window object to set.  
  
## Remarks  
 If a related CWnd object is set, the animation controller can automatically update it (send WM_PAINT message) when the status of animation manager has changed or timer post update event has occurred.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationController Class](../vs140/CAnimationController-Class.md)