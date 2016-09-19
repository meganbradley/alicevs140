---
title: "CSimpleArray::SetAtIndex"
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
ms.assetid: fca9769e-bd7e-4562-a4ed-9b91bdaf5148
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArray::SetAtIndex
Set the specified element in the array.  
  
## Syntax  
  
```  
  
      BOOL SetAtIndex(  
   int nIndex,  
   const T& t   
);  
```  
  
#### Parameters  
 `nIndex`  
 The index of the element to change.  
  
 *t*  
 The value to assign to the specified element.  
  
## Return Value  
 Returns TRUE if successful, FALSE if the index was not valid.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleArray Class](../vs140/CSimpleArray-Class.md)   
 [CSimpleArray::RemoveAt](../vs140/CSimpleArray--RemoveAt.md)   
 [CSimpleArray::Add](../vs140/CSimpleArray--Add.md)