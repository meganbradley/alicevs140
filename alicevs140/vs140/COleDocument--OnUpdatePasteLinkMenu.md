---
title: "COleDocument::OnUpdatePasteLinkMenu"
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
ms.assetid: bcb2e757-dedf-4d87-9ca7-aaa17ef8170a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::OnUpdatePasteLinkMenu
Called by the framework to determine whether a linked OLE item can be pasted from the Clipboard.  
  
## Syntax  
  
```  
  
      afx_msg void OnUpdatePasteLinkMenu(  
   CCmdUI* pCmdUI   
);  
```  
  
#### Parameters  
 `pCmdUI`  
 A pointer to a `CCmdUI` structure that represents the menu that generated the update command. The update handler calls the **Enable** member function of the `CCmdUI` structure through `pCmdUI` to update the user interface.  
  
## Remarks  
 The Paste Special menu command is enabled or disabled depending on whether the item can be pasted into the document or not.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::OnUpdatePasteMenu](../vs140/COleDocument--OnUpdatePasteMenu.md)   
 [CCmdUI Class](../vs140/CCmdUI-Class.md)