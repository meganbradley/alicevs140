---
title: "CRichEditView::SetPaperSize"
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
ms.assetid: 426647c9-b7cb-4fa4-9a90-768811437e83
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::SetPaperSize
Call this function to set the paper size for printing this rich edit view.  
  
## Syntax  
  
```  
  
      void SetPaperSize(  
   CSize sizePaper   
);  
```  
  
#### Parameters  
 *sizePaper*  
 The new paper size values for printing, measured in `MM_TWIPS`.  
  
## Remarks  
 If [m_nWordWrap](../vs140/CRichEditView--m_nWordWrap.md) is `WrapToTargetDevice`, you should call [WrapChanged](../vs140/CRichEditView--WrapChanged.md) after using this function to adjust printing characteristics.  
  
## Example  
 [!CODE [NVC_MFCDocView#161](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#161)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::GetPaperSize](../vs140/CRichEditView--GetPaperSize.md)   
 [CRichEditView::GetMargins](../vs140/CRichEditView--GetMargins.md)   
 [CRichEditView::GetPrintWidth](../vs140/CRichEditView--GetPrintWidth.md)   
 [CRichEditView::GetPrintRect](../vs140/CRichEditView--GetPrintRect.md)   
 [CRichEditView::GetPageRect](../vs140/CRichEditView--GetPageRect.md)   
 [CRichEditView::PrintPage](../vs140/CRichEditView--PrintPage.md)   
 [CRichEditView::WrapChanged](../vs140/CRichEditView--WrapChanged.md)