---
title: "CMFCVisualManager::OnDrawRibbonButtonBorder"
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
ms.assetid: 991e9c93-2a4d-4da0-aea6-a4690613e529
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonButtonBorder
The framework calls this method when it draws the border of a button on the ribbon.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonButtonBorder(  
   CDC* pDC,  
   CMFCRibbonButton* pButton  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pButton`  
 A pointer to a [CMFCRibbonButton](../vs140/CMFCRibbonButton-Class.md) object. The framework draws the border for this ribbon button.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of a `CMFCRibbonButton`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)