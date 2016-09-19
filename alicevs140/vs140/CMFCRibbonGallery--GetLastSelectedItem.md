---
title: "CMFCRibbonGallery::GetLastSelectedItem"
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
ms.assetid: eb256a3b-180d-4d42-8b8c-7d388461f3f9
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGallery::GetLastSelectedItem
Returns the index of the last item in the ribbon gallery that the user selected.  
  
## Syntax  
  
```  
static int GetLastSelectedItem(  
    UINT uiCmdID   
);  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 Specifies the command ID of the menu item that opened the ribbon gallery.  
  
## Return Value  
 When the user selects any item in the ribbon gallery, the library sends the `WM_COMMAND` message along with Command ID of the menu button that opened the ribbon gallery.  
  
## Remarks  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)