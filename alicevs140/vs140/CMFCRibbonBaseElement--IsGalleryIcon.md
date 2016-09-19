---
title: "CMFCRibbonBaseElement::IsGalleryIcon"
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
ms.assetid: ff0848ac-94aa-4a3b-9cce-62815dd9487d
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::IsGalleryIcon
Indicates whether the ribbon element is contained in a ribbon gallery.  
  
## Syntax  
  
```  
virtual BOOL IsGalleryIcon() const;  
```  
  
## Return Value  
 Always returns `FALSE`.  
  
## Remarks  
 By default this method always returns `FALSE`. Override this method in a derived class to indicate whether the ribbon element is contained in a ribbon gallery.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)