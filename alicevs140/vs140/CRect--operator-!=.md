---
title: "CRect::operator !="
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
ms.assetid: a582729a-1054-448a-958c-ded49b013282
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::operator !=
Determines whether `rect` is not equal to `CRect` by comparing the coordinates of their upper-left and lower-right corners.  
  
## Syntax  
  
```  
  
      BOOL operator!=(   
   const RECT& rect    
) const throw( );  
```  
  
#### Parameters  
 `rect`  
 Refers to a source rectangle. Can be a [RECT](../vs140/RECT-Structure.md) or `CRect`.  
  
## Return Value  
 Nonzero if not equal; otherwise 0.  
  
## Remarks  
  
> [!NOTE]
>  Both of the rectangles must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangles before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#61](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#61)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator ==](../vs140/CRect--operator-==.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)   
 [EqualRect](http://msdn.microsoft.com/library/windows/desktop/dd162699)