---
title: "CRect::IsRectEmpty"
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
ms.assetid: 1ff0b971-52d3-442e-b918-b292e6de224d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::IsRectEmpty
Determines whether `CRect` is empty.  
  
## Syntax  
  
```  
  
BOOL IsRectEmpty( ) const throw( );  
  
```  
  
## Return Value  
 Nonzero if `CRect` is empty; 0 if `CRect` is not empty.  
  
## Remarks  
 A rectangle is empty if the width and/or height are 0 or negative. Differs from `IsRectNull`, which determines whether all coordinates of the rectangle are zero.  
  
> [!NOTE]
>  The rectangle must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangle before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#44](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#44)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::IsRectNull](../vs140/CRect--IsRectNull.md)   
 [CRect::SetRectEmpty](../vs140/CRect--SetRectEmpty.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)   
 [IsRectEmpty](http://msdn.microsoft.com/library/windows/desktop/dd145017)