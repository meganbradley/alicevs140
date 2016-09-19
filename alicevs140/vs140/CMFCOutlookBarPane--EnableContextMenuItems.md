---
title: "CMFCOutlookBarPane::EnableContextMenuItems"
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
ms.assetid: d1a5dba8-c194-4324-825f-d3441e99828a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarPane::EnableContextMenuItems
Specifies which shortcut menu items are displayed in customization mode.  
  
## Syntax  
  
```  
virtual BOOL EnableContextMenuItems(  
   CMFCToolBarButton* pButton,  
   CMenu* pPopup   
);  
```  
  
#### Parameters  
 [in] `pButton`  
 A pointer to a toolbar button that a user clicked.  
  
 [in] `pPopup`  
 A pointer to the shortcut menu.  
  
## Return Value  
 Returns `TRUE` if the shortcut menu should be displayed; otherwise `FALSE`.  
  
## Remarks  
 Override this method to modify the framework standard shortcut menu that the framework displays in customization mode.  
  
 The default implementation checks the customization mode ([CMFCToolBar::IsCustomizeMode](../vs140/CMFCToolBar--IsCustomizeMode.md)) and if it is set to `TRUE`, disables all the shortcut menu items except **Delete**. Then, it just passes the input parameters to `CMFCToolBar::EnableContextMenuItems`.  
  
> [!NOTE]
>  *Context menu* is a synonym for shortcut menu.  
  
## Requirements  
 **Header:** afxoutlookbarpane.h  
  
## See Also  
 [CMFCOutlookBarPane Class](../vs140/CMFCOutlookBarPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)