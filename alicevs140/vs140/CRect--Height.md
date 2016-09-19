---
title: "CRect::Height"
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
ms.assetid: cf540367-f531-4a76-a607-3c1f6875a105
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::Height
Calculates the height of `CRect` by subtracting the top value from the bottom value.  
  
## Syntax  
  
```  
  
int Height( ) const throw( );  
  
```  
  
## Return Value  
 The height of `CRect`.  
  
## Remarks  
 The resulting value can be negative.  
  
> [!NOTE]
>  The rectangle must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangle before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#41](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#41)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::Width](../vs140/CRect--Width.md)   
 [CRect::Size](../vs140/CRect--Size.md)   
 [CRect::CenterPoint](../vs140/CRect--CenterPoint.md)   
 [CRect::IsRectEmpty](../vs140/CRect--IsRectEmpty.md)   
 [CRect::IsRectNull](../vs140/CRect--IsRectNull.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)