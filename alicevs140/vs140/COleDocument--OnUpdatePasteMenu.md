---
title: "COleDocument::OnUpdatePasteMenu"
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
ms.assetid: 65521b1d-f727-4225-916c-36524a283a00
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::OnUpdatePasteMenu
Called by the framework to determine whether an embedded OLE item can be pasted from the Clipboard.  
  
## Syntax  
  
```  
afx_msg void OnUpdatePasteMenu(  
   CCmdUI* pCmdUI   
);  
```  
  
#### Parameters  
 `pCmdUI`  
 A pointer to a `CCmdUI` structure that represents the menu that generated the update command. The update handler calls the **Enable** member function of the `CCmdUI` structure through `pCmdUI` to update the user interface.  
  
## Remarks  
 The Paste menu command and button are enabled or disabled depending on whether the item can be pasted into the document or not.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::OnUpdatePasteLinkMenu](../vs140/COleDocument--OnUpdatePasteLinkMenu.md)   
 [CCmdUI Class](../vs140/CCmdUI-Class.md)