---
title: "CEditView::GetPrinterFont"
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
ms.assetid: 625cc504-b5b5-4549-ab38-690bb2809088
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::GetPrinterFont
Call `GetPrinterFont` to get a pointer to a [CFont](../vs140/CFont-Class.md) object that describes the current printer font.  
  
## Syntax  
  
```  
  
CFont* GetPrinterFont( ) const;  
```  
  
## Return Value  
 A pointer to a `CFont` object that specifies the current printer font; **NULL** if the printer font has not been set. The pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 If the printer font has not been set, the default printing behavior of the `CEditView` class is to print using the same font used for display.  
  
 Use this function to determine the current printer font. If it is not the desired printer font, use [CEditView::SetPrinterFont](../vs140/CEditView--SetPrinterFont.md) to change it.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::SetPrinterFont](../vs140/CEditView--SetPrinterFont.md)