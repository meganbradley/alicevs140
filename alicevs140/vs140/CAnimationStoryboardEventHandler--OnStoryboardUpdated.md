---
title: "CAnimationStoryboardEventHandler::OnStoryboardUpdated"
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
ms.assetid: d4cdd973-f815-49ad-aeca-2e33d8980e16
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationStoryboardEventHandler::OnStoryboardUpdated
Handles OnStoryboardUpdated events, which occur when a storyboard is updated  
  
## Syntax  
  
```  
IFACEMETHOD(  
   OnStoryboardUpdated  
) ( __in IUIAnimationStoryboard *storyboard );  
```  
  
#### Parameters  
 `storyboard`  
 A pointer to storyboard, which was updated.  
  
## Return Value  
 S_OK if the method succeeds; otherwise E_FAIL.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationStoryboardEventHandler Class](../vs140/CAnimationStoryboardEventHandler-Class.md)