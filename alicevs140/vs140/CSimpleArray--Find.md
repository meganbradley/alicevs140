---
title: "CSimpleArray::Find"
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
ms.assetid: 595482f7-33a0-43f8-a5c9-8fddc0d9408a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArray::Find
Finds an element in the array.  
  
## Syntax  
  
```  
  
      int Find(  
   const T& t   
) const;  
```  
  
#### Parameters  
 *t*  
 The element for which to search.  
  
## Return Value  
 Returns the index of the found element, or -1 if the element is not found.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#88](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#88)]  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleArray Class](../vs140/CSimpleArray-Class.md)