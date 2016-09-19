---
title: "CSimpleArray::RemoveAt"
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
ms.assetid: 422a523f-ba3a-47fa-b04c-3ecbda3dd1fe
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArray::RemoveAt
Removes the specified element from the array.  
  
## Syntax  
  
```  
  
      BOOL RemoveAt(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 Index pointing to the element to remove.  
  
## Return Value  
 Returns TRUE if the element was removed, FALSE if the index was invalid.  
  
## Remarks  
 When an element is removed, the remaining elements in the array are renumbered to fill the empty space.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleArray Class](../vs140/CSimpleArray-Class.md)   
 [CSimpleArray::RemoveAll](../vs140/CSimpleArray--RemoveAll.md)   
 [CSimpleArray::Remove](../vs140/CSimpleArray--Remove.md)