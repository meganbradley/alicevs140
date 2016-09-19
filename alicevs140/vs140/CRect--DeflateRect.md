---
title: "CRect::DeflateRect"
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
ms.assetid: d55554cc-f9f9-4342-b127-eda50ef76037
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::DeflateRect
`DeflateRect` deflates `CRect` by moving its sides toward its center.  
  
## Syntax  
  
```  
  
      void DeflateRect(   
   int x,   
   int y    
) throw( );  
void DeflateRect(   
   SIZE size    
) throw( );  
void DeflateRect(   
   LPCRECT lpRect    
) throw( );  
void DeflateRect(   
   int l,   
   int t,   
   int r,   
   int b    
) throw( );  
```  
  
#### Parameters  
 *x*  
 Specifies the number of units to deflate the left and right sides of `CRect`.  
  
 *y*  
 Specifies the number of units to deflate the top and bottom of `CRect`.  
  
 `size`  
 A [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) or [CSize](../vs140/CSize-Class.md) that specifies the number of units to deflate `CRect`. The `cx` value specifies the number of units to deflate the left and right sides and the `cy` value specifies the number of units to deflate the top and bottom.  
  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or `CRect` that specifies the number of units to deflate each side.  
  
 *l*  
 Specifies the number of units to deflate the left side of `CRect`.  
  
 *t*  
 Specifies the number of units to deflate the top of `CRect`.  
  
 *r*  
 Specifies the number of units to deflate the right side of `CRect`.  
  
 *b*  
 Specifies the number of units to deflate the bottom of `CRect`.  
  
## Remarks  
 To do this, `DeflateRect` adds units to the left and top and subtracts units from the right and bottom. The parameters of `DeflateRect` are signed values; positive values deflate `CRect` and negative values inflate it.  
  
 The first two overloads deflate both pairs of opposite sides of `CRect` so that its total width is decreased by two times *x* (or `cx`) and its total height is decreased by two times *y* (or `cy`). The other two overloads deflate each side of `CRect` independently of the others.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#39](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#39)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::InflateRect](../vs140/CRect--InflateRect.md)   
 [CRect::operator -](../vs140/CRect--operator--.md)   
 [CRect::operator -=](../vs140/CRect--operator--=.md)   
 [InflateRect](http://msdn.microsoft.com/library/windows/desktop/dd144994)