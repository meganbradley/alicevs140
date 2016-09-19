---
title: "CRichEditView::OnPrinterChanged"
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
ms.assetid: dde9a411-8170-4ed8-be90-be76f6df07fa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnPrinterChanged
Override this function to change characteristics for this rich edit view when the printer changes.  
  
## Syntax  
  
```  
  
      virtual void OnPrinterChanged(  
   const CDC& dcPrinter   
);  
```  
  
#### Parameters  
 `dcPrinter`  
 A [CDC](../vs140/CDC-Class.md) object for the new printer.  
  
## Remarks  
 The default implementation sets the paper size to the physical height and width for the output device (printer). If there is no device context associated with `dcPrinter`, the default implementation sets the paper size to 8.5 by 11 inches.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::SetPaperSize](../vs140/CRichEditView--SetPaperSize.md)   
 [CRichEditView::WrapChanged](../vs140/CRichEditView--WrapChanged.md)