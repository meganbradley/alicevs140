---
title: "CRect::BottomRight"
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
ms.assetid: 2eb5a9da-5df8-4818-b9ea-ee1d9b458d05
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::BottomRight
The coordinates are returned as a reference to a [CPoint](../vs140/CPoint-Class.md) object that is contained in `CRect`.  
  
## Syntax  
  
```  
  
      CPoint& BottomRight( ) throw( );   
const CPoint& BottomRight( ) const throw( );  
```  
  
## Return Value  
 The coordinates of the bottom-right corner of the rectangle.  
  
## Remarks  
 You can use this function to either get or set the bottom-right corner of the rectangle. Set the corner by using this function on the left side of the assignment operator.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#35](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#35)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::TopLeft](../vs140/CRect--TopLeft.md)   
 [CPoint Class](../vs140/CPoint-Class.md)   
 [CRect::CenterPoint](../vs140/CRect--CenterPoint.md)