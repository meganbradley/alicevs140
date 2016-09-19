---
title: "CRect::operator +="
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
ms.assetid: 2ab28143-d50f-46d2-992a-ca4c7180c43c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::operator +=
The first two overloads move `CRect` by the specified offsets.  
  
## Syntax  
  
```  
  
      void operator +=(   
   POINT point    
) throw( );  
void operator +=(   
   SIZE size    
) throw( );  
void operator +=(   
   LPCRECT lpRect    
) throw( );  
```  
  
#### Parameters  
 `point`  
 A [POINT](../vs140/POINT-Structure.md) structure or [CPoint](../vs140/CPoint-Class.md) object that specifies the number of units to move the rectangle.  
  
 `size`  
 A [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or [CSize](../vs140/CSize-Class.md) object that specifies the number of units to move the rectangle.  
  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or `CRect` object that contains the number of units to inflate each side of `CRect`.  
  
## Remarks  
 The parameter's *x* and *y* (or `cx` and `cy`) values are added to `CRect`.  
  
 The third overload inflates `CRect` by the number of units specifed in each member of the parameter.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#62](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#62)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::OffsetRect](../vs140/CRect--OffsetRect.md)   
 [CRect::InflateRect](../vs140/CRect--InflateRect.md)   
 [CRect::operator +](../vs140/CRect--operator--.md)   
 [CRect::operator -=](../vs140/CRect--operator--=.md)