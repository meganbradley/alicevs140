---
title: "CRect::CenterPoint"
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
ms.assetid: 66e7b0b5-b0d2-41d2-8b3d-76e8af845ca4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::CenterPoint
Calculates the centerpoint of `CRect` by adding the left and right values and dividing by two, and adding the top and bottom values and dividing by two.  
  
## Syntax  
  
```  
  
CPoint CenterPoint( ) const throw( );  
  
```  
  
## Return Value  
 A `CPoint` object that is the centerpoint of `CRect`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#36](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#36)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::Width](../vs140/CRect--Width.md)   
 [CRect::Height](../vs140/CRect--Height.md)   
 [CRect::Size](../vs140/CRect--Size.md)   
 [CRect::TopLeft](../vs140/CRect--TopLeft.md)   
 [CRect::BottomRight](../vs140/CRect--BottomRight.md)   
 [CRect::IsRectNull](../vs140/CRect--IsRectNull.md)   
 [CPoint Class](../vs140/CPoint-Class.md)