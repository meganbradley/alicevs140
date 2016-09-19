---
title: "CRect::Size"
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
ms.assetid: 1607dc3b-e0bf-4073-b6fd-bac6970439d2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::Size
The `cx` and `cy` members of the return value contain the height and width of `CRect`.  
  
## Syntax  
  
```  
  
CSize Size( ) const throw( );  
  
```  
  
## Return Value  
 A [CSize](../vs140/CSize-Class.md) object that contains the size of `CRect`.  
  
## Remarks  
 Either the height or width can be negative.  
  
> [!NOTE]
>  The rectangle must be normalized or this function may fail. You can call [NormalizeRect](../vs140/CRect--NormalizeRect.md) to normalize the rectangle before calling this function.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#54](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#54)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::Height](../vs140/CRect--Height.md)   
 [CRect::Width](../vs140/CRect--Width.md)   
 [CRect::IsRectEmpty](../vs140/CRect--IsRectEmpty.md)   
 [CRect::IsRectNull](../vs140/CRect--IsRectNull.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)