---
title: "CDC::GetCurrentFont"
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
ms.assetid: c4fbfc39-c081-499c-bc96-f34d7ec75dde
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetCurrentFont
Returns a pointer to the currently selected `CFont` object.  
  
## Syntax  
  
```  
  
CFont* GetCurrentFont( ) const;  
```  
  
## Return Value  
 Pointer to a `CFont` object, if successful; otherwise **NULL**.  
  
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
 [CDC::GetCurrentPalette](../vs140/CDC--GetCurrentPalette.md)   
 [CDC::GetCurrentPen](../vs140/CDC--GetCurrentPen.md)