---
title: "CRect::EqualRect"
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
ms.assetid: f662ea04-e284-4d9a-9c43-83d27886376d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::EqualRect
Determines whether `CRect` is equal to the given rectangle.  
  
## Syntax  
  
```  
  
      BOOL EqualRect(   
   LPCRECT lpRect    
) const throw( );  
```  
  
#### Parameters  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or `CRect` object that contains the upper-left and lower-right corner coordinates of a rectangle.  
  
## Return Value  
 Nonzero if the two rectangles have the same top, left, bottom, and right values; otherwise 0.  
  
> [!NOTE]
>  Both of the rectangles must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangles before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#40](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#40)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator ==](../vs140/CRect--operator-==.md)   
 [CRect::operator !=](../vs140/CRect--operator-!=.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)   
 [EqualRect](http://msdn.microsoft.com/library/windows/desktop/dd162699)