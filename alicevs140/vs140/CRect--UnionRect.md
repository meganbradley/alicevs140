---
title: "CRect::UnionRect"
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
ms.assetid: 22fb6e72-1e2b-453e-a139-87869c88a3fa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::UnionRect
Makes the dimensions of `CRect` equal to the union of the two source rectangles.  
  
## Syntax  
  
```  
  
      BOOL UnionRect(   
   LPCRECT lpRect1,   
   LPCRECT lpRect2    
) throw( );  
```  
  
#### Parameters  
 `lpRect1`  
 Points to a [RECT](../vs140/RECT-Structure.md) or `CRect` that contains a source rectangle.  
  
 `lpRect2`  
 Points to a `RECT` or `CRect` that contains a source rectangle.  
  
## Return Value  
 Nonzero if the union is not empty; 0 if the union is empty.  
  
## Remarks  
 The union is the smallest rectangle that contains both source rectangles.  
  
 Windows ignores the dimensions of an empty rectangle; that is, a rectangle that has no height or has no width.  
  
> [!NOTE]
>  Both of the rectangles must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangles before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#56](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#56)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator &#124;=](../vs140/CRect--operator--=.md)   
 [CRect::operator &#124;](../vs140/CRect--operator--.md)   
 [CRect::IntersectRect](../vs140/CRect--IntersectRect.md)   
 [CRect::SubtractRect](../vs140/CRect--SubtractRect.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)   
 [UnionRect](http://msdn.microsoft.com/library/windows/desktop/dd145163)