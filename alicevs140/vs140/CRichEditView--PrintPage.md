---
title: "CRichEditView::PrintPage"
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
ms.assetid: 75db1cef-e5ab-4552-b726-3da113f61f33
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::PrintPage
Call this function to format a range of text in a rich edit control for the output device specified by `pDC`.  
  
## Syntax  
  
```  
  
      long PrintPage(  
   CDC* pDC,  
   long nIndexStart,  
   long nIndexStop   
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to a device context for page output.  
  
 `nIndexStart`  
 Zero-based index of the first character to be formatted.  
  
 `nIndexStop`  
 Zero-based index of the last character to be formatted.  
  
## Return Value  
 The index of the last character that fits on the page plus one.  
  
## Remarks  
 The layout of each page is controlled by [GetPageRect](../vs140/CRichEditView--GetPageRect.md) and [GetPrintRect](../vs140/CRichEditView--GetPrintRect.md). Typically, this call is followed by a call to [CRichEditCtrl::DisplayBand](../vs140/CRichEditCtrl--DisplayBand.md) which generates the output.  
  
 Note that margins are relative to the physical page, not the logical page. Thus, margins of zero will often clip the text since many printers have unprintable areas on the page. To avoid clipping your text, you should call [SetMargins](../vs140/CRichEditView--SetMargins.md) and set reasonable margins before printing.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::PrintInsideRect](../vs140/CRichEditView--PrintInsideRect.md)   
 [CRichEditView::GetPageRect](../vs140/CRichEditView--GetPageRect.md)   
 [CRichEditView::GetPrintRect](../vs140/CRichEditView--GetPrintRect.md)   
 [CRichEditView::SetMargins](../vs140/CRichEditView--SetMargins.md)