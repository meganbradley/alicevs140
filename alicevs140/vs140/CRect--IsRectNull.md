---
title: "CRect::IsRectNull"
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
ms.assetid: 20f0d12d-9175-4de4-8c4e-d9d3735c5162
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::IsRectNull
Determines whether the top, left, bottom, and right values of `CRect` are all equal to 0.  
  
## Syntax  
  
```  
  
BOOL IsRectNull( ) const throw( );  
  
```  
  
## Return Value  
 Nonzero if `CRect`'s top, left, bottom, and right values are all equal to 0; otherwise 0.  
  
## Remarks  
 Differs from `IsRectEmpty`, which determines whether the rectangle is empty.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#45](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#45)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::IsRectEmpty](../vs140/CRect--IsRectEmpty.md)   
 [CRect::SetRectEmpty](../vs140/CRect--SetRectEmpty.md)