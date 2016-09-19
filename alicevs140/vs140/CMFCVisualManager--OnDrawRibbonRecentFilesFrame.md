---
title: "CMFCVisualManager::OnDrawRibbonRecentFilesFrame"
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
ms.assetid: e890f1c6-383e-43bd-a788-43234952c9ce
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonRecentFilesFrame
The framework calls this method when it draws a frame around a list of recent files.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonRecentFilesFrame(  
   CDC* pDC,  
   CMFCRibbonMainPanel* pPanel,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pPanel`  
 A pointer to the **Main** panel on the ribbon.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the frame for the list of recent files.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the list of recent files.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)