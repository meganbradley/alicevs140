---
title: "CSplitterWnd::ActivateNext"
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
ms.assetid: 60a61ccd-3a08-47f6-91b3-8abd0f7af14d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::ActivateNext
Called by the framework to perform the Next Pane or Previous Pane command.  
  
## Syntax  
  
```  
  
      virtual void ActivateNext(  
   BOOL bPrev = FALSE   
);  
```  
  
#### Parameters  
 `bPrev`  
 Indicates which window to activate. **TRUE** for previous; **FALSE** for next.  
  
## Remarks  
 This member function is a high level command that is used by the [CView](../vs140/CView-Class.md) class to delegate to the `CSplitterWnd` implementation.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView Class](../vs140/CView-Class.md)   
 [CSplitterWnd::CanActivateNext](../vs140/CSplitterWnd--CanActivateNext.md)   
 [CSplitterWnd::SetActivePane](../vs140/CSplitterWnd--SetActivePane.md)