---
title: "CRect::IntersectRect"
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
ms.assetid: 6d3fa6d6-2eb6-4576-b97e-d6a4bceee462
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::IntersectRect
Makes a `CRect` equal to the intersection of two existing rectangles.  
  
## Syntax  
  
```  
  
      BOOL IntersectRect(   
   LPCRECT lpRect1,   
   LPCRECT lpRect2    
) throw( );  
```  
  
#### Parameters  
 `lpRect1`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or `CRect` object that contains a source rectangle.  
  
 `lpRect2`  
 Points to a `RECT` structure or `CRect` object that contains a source rectangle.  
  
## Return Value  
 Nonzero if the intersection is not empty; 0 if the intersection is empty.  
  
## Remarks  
 The intersection is the largest rectangle contained in both existing rectangles.  
  
> [!NOTE]
>  Both of the rectangles must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangles before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#43](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#43)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator &=](../vs140/CRect--operator--=.md)   
 [CRect::operator &](../vs140/CRect--operator--.md)   
 [CRect::UnionRect](../vs140/CRect--UnionRect.md)   
 [CRect::SubtractRect](../vs140/CRect--SubtractRect.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)   
 [IntersectRect](http://msdn.microsoft.com/library/windows/desktop/dd145001)