---
title: "CRect::operator +"
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
ms.assetid: 215ee000-bd0a-487e-a004-2daa46d5bfdd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::operator +
The first two overloads return a `CRect` object that is equal to `CRect` displaced by the specified offsets.  
  
## Syntax  
  
```  
  
      CRect operator +(   
   POINT point    
) const throw( );  
CRect operator +(   
   LPCRECT lpRect    
) const throw( );  
CRect operator +(   
   SIZE size    
) const throw( );  
```  
  
#### Parameters  
 `point`  
 A [POINT](../vs140/POINT-Structure.md) structure or [CPoint](../vs140/CPoint-Class.md) object that specifies the number of units to move the return value.  
  
 `size`  
 A [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or [CSize](../vs140/CSize-Class.md) object that specifies the number of units to move the return value.  
  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or `CRect` object that contains the number of units to inflate each side of the return value.  
  
## Return Value  
 The `CRect` resulting from moving or inflating `CRect` by the number of units specified in the parameter.  
  
## Remarks  
 The parameter's *x* and *y* (or `cx` and `cy`) parameters are added to `CRect`'s position.  
  
 The third overload returns a new `CRect` that is equal to `CRect` inflated by the number of units specifed in each member of the parameter.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#65](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#65)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator +=](../vs140/CRect--operator--=.md)   
 [CRect::operator -](../vs140/CRect--operator--.md)   
 [CRect::OffsetRect](../vs140/CRect--OffsetRect.md)   
 [CRect::InflateRect](../vs140/CRect--InflateRect.md)