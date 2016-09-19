---
title: "CMFCVisualManager::OnDrawRibbonTabsFrame"
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
ms.assetid: 33ddcd1b-c17f-410a-a3f2-49d459e870cf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonTabsFrame
The framework calls this method when it draws the frame around a set of ribbon tabs.  
  
## Syntax  
  
```  
virtual COLORREF OnDrawRibbonTabsFrame(  
   CDC* pDC,  
   CMFCRibbonBar* pWndRibbonBar,  
   CRect rectTab  
);  
```  
  
#### Parameters  
 `pDC`  
 A pointer to a device context.  
  
 `pWndRibbonBar`  
 A pointer to a [CMFCRibbonBar](../vs140/CMFCRibbonBar-Class.md) object. The framework draws the frame for this ribbon bar.  
  
 `rectTab`  
 A rectangle that specifies the boundaries of the ribbon tabs.  
  
## Return Value  
 A reserved value. By default, this method returns -1.  
  
## Remarks  
 Override this method in a derived visual manager to customize the frame around a set of tabs on the ribbon.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)