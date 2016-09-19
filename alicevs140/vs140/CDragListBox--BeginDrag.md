---
title: "CDragListBox::BeginDrag"
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
ms.assetid: 1d646268-ef92-4559-9b72-393511e4531f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDragListBox::BeginDrag
Called by the framework when an event occurs that could begin a drag operation, such as pressing the left mouse button.  
  
## Syntax  
  
```  
  
      virtual BOOL BeginDrag(  
   CPoint pt   
);  
```  
  
#### Parameters  
 `pt`  
 A [CPoint](../vs140/CPoint-Class.md) object that contains the coordinates of the item being dragged.  
  
## Return Value  
 Nonzero if dragging is allowed, otherwise 0.  
  
## Remarks  
 Override this function if you want to control what happens when a drag operation begins. The default implementation captures the mouse and stays in drag mode until the user clicks the left or right mouse button or presses ESC, at which time the drag operation is canceled.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CDragListBox Class](../vs140/CDragListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDragListBox::CancelDrag](../vs140/CDragListBox--CancelDrag.md)   
 [CDragListBox::Dragging](../vs140/CDragListBox--Dragging.md)