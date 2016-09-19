---
title: "CPoint::operator +"
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
ms.assetid: 7729efc0-c61b-4906-8b04-097d07b292b9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPoint::operator +
Use this operator to offset `CPoint` by a `CPoint` or `CSize` object, or to offset a `CRect` by a `CPoint`.  
  
## Syntax  
  
```  
  
      CPoint operator +(  
   SIZE size   
) const throw( );  
CPoint operator +(  
   POINT point   
) const throw( );  
CRect operator +(  
   const RECT* lpRect   
) const throw( );  
```  
  
#### Parameters  
 `size`  
 Contains a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or [CSize](../vs140/CSize-Class.md) object.  
  
 `point`  
 Contains a [POINT](../vs140/POINT-Structure.md) structure or [CPoint](../vs140/CPoint-Class.md) object.  
  
 `lpRect`  
 Contains a pointer to a [RECT](../vs140/RECT-Structure.md) structure or [CRect](../vs140/CRect-Class.md) object.  
  
## Return Value  
 A `CPoint` that is offset by a size, a **CPoint** that is offset by a point, or a **CRect** offset by a point.  
  
## Remarks  
 For example, using one of the first two overloads to offset the point `CPoint(25, -19)` by a point `CPoint(15, 5)` or size `CSize(15, 5)` returns the value `CPoint(40, -14)`.  
  
 Adding a rectangle to a point returns the rectangle after being offset by the **x** and **y** values specified in the point. For example, using the last overload to offset a rectangle `CRect(125, 219, 325, 419)` by a point `CPoint(25, -19)` returns `CRect(150, 200, 350, 400)`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#33](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#33)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CPoint Class](../vs140/CPoint-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPoint::operator -=](../vs140/CPoint--operator--=.md)   
 [CPoint::operator -](../vs140/CPoint--operator--.md)   
 [CPoint::operator +=](../vs140/CPoint--operator--=.md)   
 [CSize::operator +](../vs140/CSize--operator--.md)   
 [CRect::operator +](../vs140/CRect--operator--.md)   
 [CPoint::Offset](../vs140/CPoint--Offset.md)   
 [CRect::OffsetRect](../vs140/CRect--OffsetRect.md)