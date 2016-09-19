---
title: "CRichEditView::WrapChanged"
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
ms.assetid: 0519d4c6-6129-465e-abd6-28519e911951
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::WrapChanged
Call this function when the printing characteristics have changed ([SetMargins](../vs140/CRichEditView--SetMargins.md) or [SetPaperSize](../vs140/CRichEditView--SetPaperSize.md)).  
  
## Syntax  
  
```  
  
virtual void WrapChanged( );  
  
```  
  
## Remarks  
 Override this function to modify the way the rich edit view responds to changes in [m_nWordWrap](../vs140/CRichEditView--m_nWordWrap.md) or the printing characteristics ([OnPrinterChanged](../vs140/CRichEditView--OnPrinterChanged.md)).  
  
## Example  
 [!CODE [NVC_MFCDocView#163](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#163)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::m_nWordWrap](../vs140/CRichEditView--m_nWordWrap.md)   
 [CRichEditView::OnPrinterChanged](../vs140/CRichEditView--OnPrinterChanged.md)   
 [CRichEditView::SetMargins](../vs140/CRichEditView--SetMargins.md)   
 [CRichEditView::SetPaperSize](../vs140/CRichEditView--SetPaperSize.md)