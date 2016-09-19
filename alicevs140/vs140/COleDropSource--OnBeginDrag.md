---
title: "COleDropSource::OnBeginDrag"
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
ms.assetid: d997751c-b571-4846-9b46-da91f19f574c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDropSource::OnBeginDrag
Called by the framework when an event occurs that could begin a drag operation, such as pressing the left mouse button.  
  
## Syntax  
  
```  
  
      virtual BOOL OnBeginDrag(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 Points to the window that contains the selected data.  
  
## Return Value  
 Nonzero if dragging is allowed, otherwise 0.  
  
## Remarks  
 Override this function if you want to modify the way the dragging process is started. The default implementation captures the mouse and stays in drag mode until the user clicks the left or right mouse button or hits ESC, at which time it releases the mouse.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDropSource Class](../vs140/COleDropSource-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDropSource::GiveFeedback](../vs140/COleDropSource--GiveFeedback.md)