---
title: "COleDocument::OnUpdateEditLinksMenu"
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
ms.assetid: 560598b8-8c21-4bbc-9511-c32c23f1b148
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::OnUpdateEditLinksMenu
Called by the framework to update the Links command on the Edit menu.  
  
## Syntax  
  
```  
  
      afx_msg void OnUpdateEditLinksMenu(  
   CCmdUI* pCmdUI   
);  
```  
  
#### Parameters  
 `pCmdUI`  
 A pointer to a `CCmdUI` structure that represents the menu that generated the update command. The update handler calls the **Enable** member function of the `CCmdUI` structure through `pCmdUI` to update the user interface.  
  
## Remarks  
 Starting with the first OLE item in the document, `OnUpdateEditLinksMenu` accesses each item, tests whether the item is a link, and, if it is a link, enables the Links command. Override this function to change the behavior.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::OnEditLinks](../vs140/COleDocument--OnEditLinks.md)   
 [COleDocument::GetStartPosition](../vs140/COleDocument--GetStartPosition.md)   
 [COleDocument::GetNextClientItem](../vs140/COleDocument--GetNextClientItem.md)   
 [CCmdUI Class](../vs140/CCmdUI-Class.md)