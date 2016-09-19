---
title: "CRect::SubtractRect"
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
ms.assetid: cdf5359b-04fd-4e3f-8a28-ccaf7eef1bc4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::SubtractRect
Makes the dimensions of the **CRect** equal to the subtraction of `lpRectSrc2` from `lpRectSrc1`.  
  
## Syntax  
  
```  
  
      BOOL SubtractRect(   
   LPCRECT lpRectSrc1,   
   LPCRECT lpRectSrc2    
) throw( );  
```  
  
#### Parameters  
 `lpRectSrc1`  
 Points to the [RECT](../vs140/RECT-Structure.md) structure or `CRect` object from which a rectangle is to be subtracted.  
  
 `lpRectSrc2`  
 Points to the `RECT` structure or `CRect` object that is to be subtracted from the rectangle pointed to by the `lpRectSrc1` parameter.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The subtraction is the smallest rectangle that contains all of the points in `lpRectScr1` that are not in the intersection of `lpRectScr1` and *lpRectScr2*.  
  
 The rectangle specified by `lpRectSrc1` will be unchanged if the rectangle specified by `lpRectSrc2` doesn't completely overlap the rectangle specified by *lpRectSrc1* in at least one of the x- or y-directions.  
  
 For example, if `lpRectSrc1` were (10,10, 100,100) and `lpRectSrc2` were (50,50, 150,150), the rectangle pointed to by `lpRectSrc1` would be unchanged when the function returned. If `lpRectSrc1` were (10,10, 100,100) and `lpRectSrc2` were (50,10, 150,150), however, the rectangle pointed to by `lpRectSrc1` would contain the coordinates (10,10, 50,100) when the function returned.  
  
 `SubtractRect` is not the same as [operator -](../vs140/CRect--operator--.md) nor [operator -=](../vs140/CRect--operator--=.md). Neither of these operators ever calls `SubtractRect`.  
  
> [!NOTE]
>  Both of the rectangles must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangles before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#55](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#55)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator -](../vs140/CRect--operator--.md)   
 [CRect::operator -=](../vs140/CRect--operator--=.md)   
 [CRect::IntersectRect](../vs140/CRect--IntersectRect.md)   
 [CRect::UnionRect](../vs140/CRect--UnionRect.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)   
 [SubtractRect](http://msdn.microsoft.com/library/windows/desktop/dd145125)