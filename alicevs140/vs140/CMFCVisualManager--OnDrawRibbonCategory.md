---
title: "CMFCVisualManager::OnDrawRibbonCategory"
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
ms.assetid: a6309724-b13e-441b-8ba1-05428cfa95b5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonCategory
The framework calls this method when it draws a [CMFCRibbonCategory](../vs140/CMFCRibbonCategory-Class.md) object.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonCategory(  
   CDC* pDC,  
   CMFCRibbonCategory* pCategory,  
   CRect rectCategory  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pCategory`  
 A pointer to a `CMFCRibbonCategory` object. The framework draws this ribbon category.  
  
 [in] `rectCategory`  
 A rectangle that specifies the boundary of all the category panels on the ribbon.  
  
## Remarks  
 A ribbon category is a logical grouping of menu commands. For more information about ribbon categories, see [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md).  
  
 Override this method in a derived visual manager to customize the appearance of a ribbon category.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)