---
title: "CRichEditView::GetPaperSize"
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
ms.assetid: b7c2a231-9c30-47b7-a888-2508a2c2a716
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetPaperSize
Call this function to retrieve the current paper size.  
  
## Syntax  
  
```  
  
CSize GetPaperSize( ) const;  
  
```  
  
## Return Value  
 The size of the paper used in printing, measured in `MM_TWIPS`.  
  
## Example  
 [!CODE [NVC_MFCDocView#153](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#153)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::SetPaperSize](../vs140/CRichEditView--SetPaperSize.md)   
 [CRichEditView::GetMargins](../vs140/CRichEditView--GetMargins.md)   
 [CRichEditView::GetPrintWidth](../vs140/CRichEditView--GetPrintWidth.md)   
 [CRichEditView::GetPrintRect](../vs140/CRichEditView--GetPrintRect.md)   
 [CRichEditView::GetPageRect](../vs140/CRichEditView--GetPageRect.md)   
 [CRichEditView::PrintPage](../vs140/CRichEditView--PrintPage.md)