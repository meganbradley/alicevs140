---
title: "CMFCVisualManager::OnFillHeaderCtrlBackground"
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
ms.assetid: 8ac40dd2-6477-4cd4-af77-93bad1c0a7aa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillHeaderCtrlBackground
The framework calls this method when it fills the background of a header control.  
  
## Syntax  
  
```  
virtual void OnFillHeaderCtrlBackground(  
   CMFCHeaderCtrl* pCtrl,  
   CDC* pDC,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pCtrl`  
 A pointer to a [CMFCHeaderCtrl](../vs140/CMFCHeaderCtrl-Class.md) object. The framework fills the background for this header control.  
  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the header control.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of a header control.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCHeaderCtrl Class](../vs140/CMFCHeaderCtrl-Class.md)