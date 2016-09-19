---
title: "CPaneFrameWnd::OnCheckRollState"
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
ms.assetid: 108b3641-b603-48a1-b567-80f215f7346d
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::OnCheckRollState
Determines whether a mini-frame window should be rolled up or down.  
  
## Syntax  
  
```  
virtual void OnCheckRollState();  
```  
  
## Remarks  
 This method is called by the framework to determine whether a mini-frame window should be rolled up or down.  
  
 By default, the framework calls [CPaneFrameWnd::IsRollUp](../vs140/CPaneFrameWnd--IsRollUp.md) and [CPaneFrameWnd::IsRollDown](../vs140/CPaneFrameWnd--IsRollDown.md) and just stretches or restores the mini-frame window. You can override this method in a derived class to use a different visual effect.  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)