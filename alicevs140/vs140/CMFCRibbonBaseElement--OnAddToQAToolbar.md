---
title: "CMFCRibbonBaseElement::OnAddToQAToolbar"
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
ms.assetid: ea2a4544-d80a-4602-b1fc-0bebf88db77f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::OnAddToQAToolbar
Adds the ribbon element to the specified quick access toolbar.  
  
## Syntax  
  
```  
virtual BOOL OnAddToQAToolbar(  
   CMFCRibbonQuickAccessToolBar& qat  
);  
```  
  
#### Parameters  
 [in] `qat`  
 The quick access toolbar.  
  
## Return Value  
 Always returns `TRUE` indicating the ribbon element was added to the quick access toolbar.  
  
## Remarks  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)