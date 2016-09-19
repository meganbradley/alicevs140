---
title: "CRichEditView::GetPrintRect"
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
ms.assetid: bbd46268-e0e8-4578-bce2-357e8dd83fa7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetPrintRect
Call this function to retrieve the bounds of the printing area within the page rectangle.  
  
## Syntax  
  
```  
  
CRect GetPrintRect( ) const;  
  
```  
  
## Return Value  
 The bounds of the image area used in printing, measured in `MM_TWIPS`.  
  
## Example  
 [!CODE [NVC_MFCDocView#154](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#154)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::GetMargins](../vs140/CRichEditView--GetMargins.md)   
 [CRichEditView::GetPrintWidth](../vs140/CRichEditView--GetPrintWidth.md)   
 [CRichEditView::GetPaperSize](../vs140/CRichEditView--GetPaperSize.md)   
 [CRichEditView::GetPageRect](../vs140/CRichEditView--GetPageRect.md)   
 [CRichEditView::PrintPage](../vs140/CRichEditView--PrintPage.md)