---
title: "CMFCRibbonBaseElement::OnAutoRepeat"
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
ms.assetid: a2f3a655-6265-49d3-956a-cf97e658df82
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::OnAutoRepeat
Updates the ribbon element in response to sustained user input.  
  
## Syntax  
  
```  
virtual BOOL OnAutoRepeat();  
```  
  
## Return Value  
 Always returns `FALSE`.  
  
## Remarks  
 By default this method always return `FALSE`. Override this method to process sustained user input.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)