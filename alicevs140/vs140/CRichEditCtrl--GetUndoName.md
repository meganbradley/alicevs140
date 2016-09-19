---
title: "CRichEditCtrl::GetUndoName"
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
ms.assetid: 16294a52-255b-4eba-9a11-737e6d6587cb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetUndoName
Retrieves the type of the next available action in the undo queue, if any.  
  
## Syntax  
  
```  
  
UNDONAMEID GetUndoName( ) const;  
  
```  
  
## Return Value  
 If an undo action is in the control's undo queue, `GetUndoName` returns the [UNDONAMEID](http://msdn.microsoft.com/library/windows/desktop/bb774365) enumeration type indicating the type of the next action in the queue. If the undo queue is empty, or if the undo action in the queue is of an unknown type, `GetUndoName` returns 0.  
  
## Remarks  
 The types of actions that can be undone or redone include typing, delete, drag-drop, cut, and paste operations. This information can be useful for applications that provide an extended user interface for Undo and Redo operations, such as a drop-down list box of actions that can be undone.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)   
 [CRichEditCtrl::Redo](../vs140/CRichEditCtrl--Redo.md)   
 [CRichEditCtrl::GetRedoName](../vs140/CRichEditCtrl--GetRedoName.md)