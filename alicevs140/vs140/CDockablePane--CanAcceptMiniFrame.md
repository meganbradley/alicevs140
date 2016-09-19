---
title: "CDockablePane::CanAcceptMiniFrame"
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
ms.assetid: e95570e1-1622-4a71-a7f3-3bd7a41d9602
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::CanAcceptMiniFrame
Determines whether the specified mini-frame can be docked to the pane.  
  
## Syntax  
  
```  
virtual BOOL CanAcceptMiniFrame(  
   CPaneFrameWnd* pMiniFrame  
) const;  
```  
  
#### Parameters  
 [in] `pMiniFrame`  
 Pointer to a `CPaneFrameWnd` object.  
  
## Return Value  
 `TRUE` if `pMiniFrame` can be docked to the pane; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [CDockablePane::CanAcceptPane](../vs140/CDockablePane--CanAcceptPane.md)