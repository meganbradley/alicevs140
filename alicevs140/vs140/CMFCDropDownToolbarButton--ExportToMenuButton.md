---
title: "CMFCDropDownToolbarButton::ExportToMenuButton"
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
ms.assetid: 8f254ad4-41e5-471c-bf57-2cffa81df11a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::ExportToMenuButton
Copies text from the toolbar button to a menu.  
  
## Syntax  
  
```  
virtual BOOL ExportToMenuButton(  
   CMFCToolBarMenuButton& menuButton  
) const;  
```  
  
#### Parameters  
 [in] `menuButton`  
 A reference to the target menu button.  
  
## Return Value  
 Nonzero if the method succeeds; otherwise 0.  
  
## Remarks  
 This method calls the base class implementation ([CMFCToolBarButton::ExportToMenuButton](../vs140/CMFCToolBarButton--ExportToMenuButton.md)) and then appends to the target menu button a pop-up menu that contains each toolbar menu item in this button. This method does not append sub-menus to the pop-up menu.  
  
 This method fails if the parent toolbar, `m_pToolBar`, is `NULL` or the base class implementation returns `FALSE`.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::ExportToMenuButton](../vs140/CMFCToolBarButton--ExportToMenuButton.md)