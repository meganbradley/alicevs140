---
title: "CRect::NormalizeRect"
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
ms.assetid: 0c8fd2fa-53bd-4218-abd6-11923eef7d01
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::NormalizeRect
Normalizes `CRect` so that both the height and width are positive.  
  
## Syntax  
  
```  
  
void NormalizeRect( ) throw( );  
  
```  
  
## Remarks  
 The rectangle is normalized for fourth-quadrant positioning, which Windows typically uses for coordinates. `NormalizeRect` compares the top and bottom values, and swaps them if the top is greater than the bottom. Similarly, it swaps the left and right values if the left is greater than the right. This function is useful when dealing with different mapping modes and inverted rectangles.  
  
> [!NOTE]
>  The following `CRect` member functions require normalized rectangles in order to work properly: [Height](../vs140/CRect--Height.md), [Width](../vs140/CRect--Width.md), [Size](../vs140/CRect--Size.md), [IsRectEmpty](../vs140/CRect--IsRectEmpty.md), [PtInRect](../vs140/CRect--PtInRect.md), [EqualRect](../vs140/CRect--EqualRect.md), [UnionRect](../vs140/CRect--UnionRect.md), [IntersectRect](../vs140/CRect--IntersectRect.md), [SubtractRect](../vs140/CRect--SubtractRect.md), [operator ==](../vs140/CRect--operator-==.md), [operator !=](../vs140/CRect--operator-!=.md), [operator &#124;](../vs140/CRect--operator--.md), [operator &#124;=](../vs140/CRect--operator--=.md), [operator &](../vs140/CRect--operator--.md), and [operator &=](../vs140/CRect--operator--=.md).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#49](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#49)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)