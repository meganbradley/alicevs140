---
title: "Tree Control Notification Messages"
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
ms.topic: article
ms.assetid: ac7013b4-91dd-4668-bd75-439ca0680ef9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Tree Control Notification Messages
A tree control ([CTreeCtrl](../vs140/CTreeCtrl-Class.md)) sends the following notification messages as **WM_NOTIFY** messages:  
  
|Notification message|Description|  
|--------------------------|-----------------|  
|**TVN_BEGINDRAG**|Signals the start of a drag-and-drop operation|  
|**TVN_BEGINLABELEDIT**|Signals the start of in-place label editing|  
|**TVN_BEGINRDRAG**|Signals the start of a drag-and-drop operation, using the right mouse button|  
|**TVN_DELETEITEM**|Signals the deletion of a specific item|  
|**TVN_ENDLABELEDIT**|Signals the end of label editing|  
|**TVN_GETDISPINFO**|Requests information that the tree control requires to display an item|  
|**TVN_ITEMEXPANDED**|Signals that a parent item's list of child items was expanded or collapsed|  
|**TVN_ITEMEXPANDING**|Signals that a parent item's list of child items is about to be expanded or collapsed|  
|**TVN_KEYDOWN**|Signals a keyboard event|  
|**TVN_SELCHANGED**|Signals that the selection has changed from one item to another|  
|**TVN_SELCHANGING**|Signals that the selection is about to be changed from one item to another|  
|**TVN_SETDISPINFO**|Notification to update the information maintained for an item|  
  
## See Also  
 [Using CTreeCtrl](../vs140/Using-CTreeCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)