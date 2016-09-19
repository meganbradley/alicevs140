---
title: "CRichEditCtrl::SetUndoLimit"
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
ms.assetid: f61f5e5c-b606-46d4-bf61-d55c3e65d733
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetUndoLimit
Sets the maximum number of actions that can stored in the undo queue.  
  
## Syntax  
  
```  
  
      UINT SetUndoLimit(  
   UINT nLimit   
);  
```  
  
#### Parameters  
 *nLimit*  
 Specifies the maximum number of actions that can be stored in the undo queue. Set to zero to disable Undo.  
  
## Return Value  
 The new maximum number of undo actions for the rich edit control.  
  
## Remarks  
 By default, the maximum number of actions in the undo queue is 100. If you increase this number, there must be enough available memory to accommodate the new number. For better performance, set the limit to the smallest possible value.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::EmptyUndoBuffer](../vs140/CRichEditCtrl--EmptyUndoBuffer.md)   
 [CRichEditCtrl::Undo](../vs140/CRichEditCtrl--Undo.md)