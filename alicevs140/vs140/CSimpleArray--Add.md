---
title: "CSimpleArray::Add"
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
ms.assetid: 0bf3ffa0-69e8-43d3-999a-f8138ae729e2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArray::Add
Adds a new element to the array.  
  
## Syntax  
  
```  
  
      BOOL Add(  
   const T& t   
);  
```  
  
#### Parameters  
 *t*  
 The element to add to the array.  
  
## Return Value  
 Returns TRUE if the element is successfully added to the array, FALSE otherwise.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#87](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#87)]  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleArray Class](../vs140/CSimpleArray-Class.md)   
 [CSimpleArray::SetAtIndex](../vs140/CSimpleArray--SetAtIndex.md)