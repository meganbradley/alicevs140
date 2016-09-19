---
title: "CMFCRibbonBaseElement::Redraw"
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
ms.assetid: f97dd7b9-dd71-4621-8a00-c982a591b807
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::Redraw
Updates the display for the ribbon element.  
  
## Syntax  
  
```  
virtual void Redraw();  
```  
  
## Remarks  
 This method redraws the display rectangle for the ribbon element by calling [CWnd::RedrawWindow](http://msdn.microsoft.com/library/windows/desktop/dd162911) with the `RDW_INVALIDATE`, `RDW_ERASE`, and `RDW_UPDATENOW` flags set.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)