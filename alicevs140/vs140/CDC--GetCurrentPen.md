---
title: "CDC::GetCurrentPen"
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
ms.assetid: 7598e774-69f3-4261-aed5-71df44c757bd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetCurrentPen
Returns a pointer to the currently selected `CPen` object.  
  
## Syntax  
  
```  
  
CPen* GetCurrentPen( ) const;  
```  
  
## Return Value  
 Pointer to a `CPen` object, if successful; otherwise **NULL**.  
  
## Remarks  
 This member function may return temporary objects.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SelectObject](../vs140/CDC--SelectObject.md)   
 [GetCurrentObject](http://msdn.microsoft.com/library/windows/desktop/dd144869)   
 [CDC::GetCurrentBitmap](../vs140/CDC--GetCurrentBitmap.md)   
 [CDC::GetCurrentBrush](../vs140/CDC--GetCurrentBrush.md)   
 [CDC::GetCurrentFont](../vs140/CDC--GetCurrentFont.md)   
 [CDC::GetCurrentPalette](../vs140/CDC--GetCurrentPalette.md)