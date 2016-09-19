---
title: "CMFCDropDownToolbarButton::OnCustomizeMenu"
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
ms.assetid: db44ea1c-96c5-484d-b614-dc79f18b7886
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::OnCustomizeMenu
Modifies the provided menu when the application displays a shortcut menu on the parent toolbar.  
  
## Syntax  
  
```  
virtual BOOL OnCustomizeMenu(  
   CMenu* pMenu  
);  
```  
  
#### Parameters  
 [in] `pMenu`  
 The menu to customize.  
  
## Return Value  
 This method returns `TRUE`.  
  
## Remarks  
 This method extends the base class implementation ([CMFCToolBarButton::OnCustomizeMenu](../vs140/CMFCToolBarButton--OnCustomizeMenu.md)) by disabling the following menu items:  
  
-   **Copy Button Image**  
  
-   **Button Appearance**  
  
-   **Image**  
  
-   **Text**  
  
-   **Image and Text**  
  
 Override this method to modify the shortcut menu that the framework displays in customization mode.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnCustomizeMenu](../vs140/CMFCToolBarButton--OnCustomizeMenu.md)