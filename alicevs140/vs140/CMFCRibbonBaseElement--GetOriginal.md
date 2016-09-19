---
title: "CMFCRibbonBaseElement::GetOriginal"
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
ms.assetid: 27b75a06-a095-44c0-9ca0-5d1666095b93
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::GetOriginal
Retrieves the original ribbon element.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* GetOriginal() const;  
```  
  
## Return Value  
 A pointer to the original ribbon element.  
  
## Remarks  
 Ribbon elements that are copied to another container retain a pointer to the original ribbon element.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)