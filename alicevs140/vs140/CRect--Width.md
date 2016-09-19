---
title: "CRect::Width"
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
ms.assetid: 3f561b92-c6dc-4597-9dd8-12cd60a45d7b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::Width
Calculates the width of `CRect` by subtracting the left value from the right value.  
  
## Syntax  
  
```  
  
int Width( ) const throw( );  
  
```  
  
## Return Value  
 The width of `CRect`.  
  
## Remarks  
 The width can be negative.  
  
> [!NOTE]
>  The rectangle must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangle before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#57](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#57)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::Height](../vs140/CRect--Height.md)   
 [CRect::Size](../vs140/CRect--Size.md)   
 [CRect::CenterPoint](../vs140/CRect--CenterPoint.md)   
 [CRect::IsRectEmpty](../vs140/CRect--IsRectEmpty.md)   
 [CRect::IsRectNull](../vs140/CRect--IsRectNull.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)