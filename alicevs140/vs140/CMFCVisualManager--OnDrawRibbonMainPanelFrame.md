---
title: "CMFCVisualManager::OnDrawRibbonMainPanelFrame"
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
ms.assetid: d56fc51c-9648-4731-b652-cf0078434872
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonMainPanelFrame
The framework calls this method when it draws the frame around the [CMFCRibbonMainPanel](../vs140/CMFCRibbonMainPanel-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawRibbonMainPanelFrame(  
   CDC* pDC,  
   CMFCRibbonMainPanel* pPanel,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pPanel`  
 A pointer to the `CMFCRibbonMainPanel`.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the `CMFCRibbonMainPanel`.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the frame for the `CMFCRibbonMainPanel`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonMainPanel Class](../vs140/CMFCRibbonMainPanel-Class.md)