---
title: "CMFCVisualManager::OnDrawRibbonStatusBarPane"
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
ms.assetid: fae3a8d3-9151-4ffd-a5a4-eb92373aaae9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonStatusBarPane
The framework calls this method when it draws a pane on the status bar.  
  
## Syntax  
  
```  
virtual COLORREF OnDrawRibbonStatusBarPane(  
   CDC* pDC,  
   CMFCRibbonStatusBar* pBar,  
   CMFCRibbonStatusBarPane* pPane  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pBar`  
 A pointer to the status bar that contains the pane.  
  
 [in] `pPane`  
 A pointer to a status bar pane. The framework draws this [CMFCRibbonStatusBarPane](../vs140/CMFCRibbonStatusBarPane-Class.md) object.  
  
## Return Value  
 A reserved value. The default implementation returns -1.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of a pane on the status bar.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonStatusBarPane Class](../vs140/CMFCRibbonStatusBarPane-Class.md)