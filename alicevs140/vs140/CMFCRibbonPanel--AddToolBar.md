---
title: "CMFCRibbonPanel::AddToolBar"
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
ms.assetid: c120bec1-5b81-487b-921f-52cc7cee47bb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::AddToolBar
Adds a toolbar to the ribbon panel.  
  
## Syntax  
  
```  
CMFCRibbonButtonsGroup* AddToolBar(  
    UINT uiToolbarResID,  
    UINT uiColdResID = 0,  
    UINT uiHotResID = 0,  
    UINT uiDisabledResID = 0  
);  
```  
  
#### Parameters  
 [in] `uiToolbarResID`  
 Specifies the resource ID of the toolbar to add.  
  
 [in] `uiColdResID`  
 Specifies the resource ID of the toolbar's cold images.  
  
 [in] `uiHotResID`  
 Specifies the resource ID of the toolbar's hot images.  
  
 [in] `uiDisabledResID`  
 Specifies the resource ID of the toolbar's disabled images.  
  
## Return Value  
 Call this method to add a toolbar to the ribbon panel. The toolbar will be added next to the ribbon element added by the previous call to [CMFCRibbonPanel::Add](../vs140/CMFCRibbonPanel--Add.md).  
  
## Remarks  
 For more information about toolbars, hot images, cold images, and disabled images, see [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md).  
  
## Requirements  
 **Header:** afxRibbonPanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)