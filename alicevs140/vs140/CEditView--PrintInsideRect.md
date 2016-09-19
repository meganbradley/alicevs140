---
title: "CEditView::PrintInsideRect"
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
ms.assetid: 34bb6c2d-d6e7-4de7-8c64-947b5517d8a0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::PrintInsideRect
Call `PrintInsideRect` to print text in the rectangle specified by *rectLayout*.  
  
## Syntax  
  
```  
  
      UINT PrintInsideRect(  
   CDC *pDC,  
   RECT& rectLayout,  
   UINT nIndexStart,  
   UINT nIndexStop   
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to the printer device context.  
  
 *rectLayout*  
 Reference to a [CRect](../vs140/CRect-Class.md) object or [RECT](../vs140/RECT-Structure.md) structure specifying the rectangle in which the text is to be rendered.  
  
 `nIndexStart`  
 Index within the buffer of the first character to be rendered.  
  
 `nIndexStop`  
 Index within the buffer of the character following the last character to be rendered.  
  
## Return Value  
 The index of the next character to be printed (that is, the character following the last character rendered).  
  
## Remarks  
 If the `CEditView` control does not have the style **ES_AUTOHSCROLL**, text is wrapped within the rendering rectangle. If the control does have the style **ES_AUTOHSCROLL**, the text is clipped at the right edge of the rectangle.  
  
 The **rect.bottom** element of the *rectLayout* object is changed so that the rectangle's dimensions define the part of the original rectangle that is occupied by the text.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::SetPrinterFont](../vs140/CEditView--SetPrinterFont.md)   
 [CEditView::GetPrinterFont](../vs140/CEditView--GetPrinterFont.md)