---
title: "CMFCVisualManager::OnDrawRibbonQuickAccessToolBarSeparator"
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
ms.assetid: 8bb0f823-8285-48f9-8f15-6773707d3419
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonQuickAccessToolBarSeparator
The framework calls this method when it draws a separator on the **Quick Access Toolbar** of a ribbon.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonQuickAccessToolBarSeparator(  
   CDC* pDC,  
   CMFCRibbonSeparator* pSeparator,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pSeparator`  
 A pointer to a [CMFCRibbonSeparator](../vs140/CMFCRibbonSeparator-Class.md) object. The framework draws this ribbon separator.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the separator.  
  
## Remarks  
 Override this method in a derived class to customize the appearance of ribbon separators on the **Quick Access Toolbar**.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonSeparator Class](../vs140/CMFCRibbonSeparator-Class.md)