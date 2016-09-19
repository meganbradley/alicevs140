---
title: "CSplitterWnd::CanActivateNext"
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
ms.assetid: 0ffd9d1d-0851-428d-a880-3f06f2314a79
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::CanActivateNext
Called by the framework to check to see if the Next Pane or Previous Pane command is currently possible.  
  
## Syntax  
  
```  
  
      virtual BOOL CanActivateNext(  
   BOOL bPrev = FALSE   
);  
```  
  
#### Parameters  
 `bPrev`  
 Indicates which window to activate. **TRUE** for previous; **FALSE** for next.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function is a high level command that is used by the [CView](../vs140/CView-Class.md) class to delegate to the `CSplitterWnd` implementation.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::ActivateNext](../vs140/CSplitterWnd--ActivateNext.md)   
 [CSplitterWnd::SetActivePane](../vs140/CSplitterWnd--SetActivePane.md)