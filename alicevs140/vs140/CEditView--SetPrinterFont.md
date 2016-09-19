---
title: "CEditView::SetPrinterFont"
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
ms.assetid: e3d5a885-c5ae-4e2b-94c7-d52099ee04e4
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::SetPrinterFont
Call `SetPrinterFont` to set the printer font to the font specified by `pFont`.  
  
## Syntax  
  
```  
  
      void SetPrinterFont(  
   CFont* pFont   
);  
```  
  
#### Parameters  
 `pFont`  
 A pointer to an object of type `CFont`. If **NULL**, the font used for printing is based on the display font.  
  
## Remarks  
 If you want your view to always use a particular font for printing, include a call to `SetPrinterFont` in your class's `OnPreparePrinting` function. This virtual function is called before printing occurs, so the font change takes place before the view's contents are printed.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetFont](../vs140/CWnd--SetFont.md)   
 [CFont Class](../vs140/CFont-Class.md)   
 [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md)