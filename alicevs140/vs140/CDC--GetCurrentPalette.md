---
title: "CDC::GetCurrentPalette"
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
ms.assetid: 7afb12a8-dbfe-4f1c-955a-631f30fd6ab0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetCurrentPalette
Returns a pointer to the currently selected `CPalette` object.  
  
## Syntax  
  
```  
  
CPalette* GetCurrentPalette( ) const;  
```  
  
## Return Value  
 Pointer to a `CPalette` object, if successful; otherwise **NULL**.  
  
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
 [CDC::GetCurrentPen](../vs140/CDC--GetCurrentPen.md)