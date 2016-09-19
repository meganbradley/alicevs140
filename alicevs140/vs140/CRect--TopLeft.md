---
title: "CRect::TopLeft"
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
ms.assetid: 2cc40f1a-5117-4d22-b553-f0f32c2ff83d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::TopLeft
The coordinates are returned as a reference to a [CPoint](../vs140/CPoint-Class.md) object that is contained in `CRect`.  
  
## Syntax  
  
```  
  
      CPoint& TopLeft( ) throw( );   
const CPoint& TopLeft( ) const throw( );  
```  
  
## Return Value  
 The coordinates of the top-left corner of the rectangle.  
  
## Remarks  
 You can use this function to either get or set the top-left corner of the rectangle. Set the corner by using this function on the left side of the assignment operator.  
  
## Example  
 See the example for [CRect::CenterPoint](../vs140/CRect--CenterPoint.md).  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::BottomRight](../vs140/CRect--BottomRight.md)   
 [CPoint Class](../vs140/CPoint-Class.md)   
 [CRect::CenterPoint](../vs140/CRect--CenterPoint.md)