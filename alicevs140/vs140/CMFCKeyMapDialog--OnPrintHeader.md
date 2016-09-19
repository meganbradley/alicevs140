---
title: "CMFCKeyMapDialog::OnPrintHeader"
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
ms.assetid: 1ed897ca-2c83-4dd8-8b59-0e16e9e34f16
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCKeyMapDialog::OnPrintHeader
Called by the framework to print the header for the keyboard map on a new page.  
  
## Syntax  
  
```  
virtual int OnPrintHeader(  
   CDC& dc,  
   int nPage,  
   int cx   
) const;  
```  
  
#### Parameters  
 [in] `dc`  
 The device context for the printer.  
  
 [in] `nPage`  
 The page number to print.  
  
 [in] `cx`  
 The horizontal offset of the header, in pixels.  
  
## Return Value  
 If successful, the height of the printed text. For more information, see the Return Value section of [CDC::DrawText](../vs140/CDC--DrawText.md).  
  
## Remarks  
 The framework uses this method to print the keyboard map. By default, this method prints the page number, application name, and dialog box title.  
  
## Requirements  
 **Header:** afxkeymapdialog.h  
  
## See Also  
 [CMFCKeyMapDialog Class](../vs140/CMFCKeyMapDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::DrawText](../vs140/CDC--DrawText.md)