---
title: "CRichEditView::PrintInsideRect"
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
ms.assetid: c5403f6c-aa86-496f-9a2e-ee8090d60f2c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::PrintInsideRect
Call this function to format a range of text in a rich edit control to fit within *rectLayout* for the device specified by `pDC`.  
  
## Syntax  
  
```  
  
      long PrintInsideRect(  
   CDC* pDC,  
   RECT& rectLayout,  
   long nIndexStart,  
   long nIndexStop,  
   BOOL bOutput   
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to a device context for the output area.  
  
 *rectLayout*  
 [RECT](../vs140/RECT-Structure.md) or [CRect](../vs140/CRect-Class.md) which defines the output area.  
  
 `nIndexStart`  
 Zero-based index of the first character to be formatted.  
  
 `nIndexStop`  
 Zero-based index of the last character to be formatted.  
  
 *bOutput*  
 Indicates if the text should be rendered. If **FALSE**, the text is just measured.  
  
## Return Value  
 The index of the last character that fits in the output area plus one.  
  
## Remarks  
 Typically, this call is followed by a call to [CRichEditCtrl::DisplayBand](../vs140/CRichEditCtrl--DisplayBand.md) which generates the output.  
  
## Example  
 See the example for [CRichEditView::GetPaperSize](../vs140/CRichEditView--GetPaperSize.md).  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::FormatRange](../vs140/CRichEditCtrl--FormatRange.md)   
 [CRichEditView::PrintPage](../vs140/CRichEditView--PrintPage.md)   
 [CRichEditCtrl::DisplayBand](../vs140/CRichEditCtrl--DisplayBand.md)