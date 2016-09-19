---
title: "CMFCVisualManager::OnFillAutoHideButtonBackground"
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
ms.assetid: 72668577-00ed-4afb-89c8-c4c975aef4a9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillAutoHideButtonBackground
The framework calls this method when it fills the background of an auto-hide button.  
  
## Syntax  
  
```  
virtual void OnFillAutoHideButtonBackground(  
   CDC* pDC,  
   CRect rect,  
   CMFCAutoHideButton* pButton  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the auto-hide button.  
  
 [in] `pButton`  
 A pointer to a [CMFCAutoHideButton](../vs140/CMFCAutoHideButton-Class.md) object. The framework fills the background for this auto-hide button.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of an auto-hide button.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)