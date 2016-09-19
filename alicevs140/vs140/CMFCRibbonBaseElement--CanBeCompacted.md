---
title: "CMFCRibbonBaseElement::CanBeCompacted"
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
ms.assetid: 6a737746-14f2-47f1-8d54-9dd2faf81d78
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::CanBeCompacted
Indicates whether the size of the ribbon element can be compact.  
  
## Syntax  
  
```  
virtual BOOL CanBeCompacted() const;  
```  
  
## Return Value  
 `TRUE` if the size of the ribbon element can be compact; otherwise, `FALSE`.  
  
## Remarks  
 The size of a ribbon element can be compact, intermediate, or large.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)