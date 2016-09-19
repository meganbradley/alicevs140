---
title: "CMFCVisualManager::OnFillPopupWindowBackground"
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
ms.assetid: 8bb5cd0c-774d-4f34-b711-454e663f061b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillPopupWindowBackground
The framework calls this method when it fills the background of a pop-up window.  
  
## Syntax  
  
```  
virtual void OnFillPopupWindowBackground(  
   CDC* pDC,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the popup window.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of pop-up windows.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)