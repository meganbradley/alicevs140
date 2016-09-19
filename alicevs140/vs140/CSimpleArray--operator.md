---
title: "CSimpleArray::operator"
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
ms.assetid: 074a23c8-e767-4461-8785-2b9c19cdb043
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArray::operator
Retrieves an element from the array.  
  
## Syntax  
  
```  
  
      T& operator[](int nIndex);  
```  
  
#### Parameters  
 `nIndex`  
 The element index.  
  
## Return Value  
 Returns the element of the array referenced by `nIndex`.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#89](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#89)]  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleArray Class](../vs140/CSimpleArray-Class.md)