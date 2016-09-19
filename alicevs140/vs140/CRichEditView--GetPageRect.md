---
title: "CRichEditView::GetPageRect"
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
ms.assetid: a7ae0ca0-57bb-4312-a3e3-7910f4fefc92
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetPageRect
Call this function to get the dimensions of the page used in printing.  
  
## Syntax  
  
```  
  
CRect GetPageRect( ) const;  
  
```  
  
## Return Value  
 The bounds of the page used in printing, measured in `MM_TWIPS`.  
  
## Remarks  
 This value is based on the paper size.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::GetMargins](../vs140/CRichEditView--GetMargins.md)   
 [CRichEditView::GetPrintWidth](../vs140/CRichEditView--GetPrintWidth.md)   
 [CRichEditView::GetPrintRect](../vs140/CRichEditView--GetPrintRect.md)   
 [CRichEditView::GetPaperSize](../vs140/CRichEditView--GetPaperSize.md)   
 [CRichEditView::PrintPage](../vs140/CRichEditView--PrintPage.md)