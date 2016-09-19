---
title: "CMFCVisualManager::OnDrawRibbonDefaultPaneButton"
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
ms.assetid: f487081e-24a6-4862-820b-cbf9c4f4eace
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonDefaultPaneButton
The framework calls this method when it draws the default button for the ribbon pane.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonDefaultPaneButton(  
   CDC* pDC,  
   CMFCRibbonButton* pButton  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pButton`  
 A pointer to the default button for the ribbon pane.  
  
## Remarks  
 The framework displays the default button when a ribbon pane is resized to its minimal size and there is no area to display the content for the panel. When the user clicks on the default button, the framework displays a drop down menu that contains the content for the panel.  
  
 Override this method in a derived visual manager to customize the appearance of the default button.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)