---
title: "shared_future::operator= Operator"
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
ms.topic: article
ms.assetid: dabf7d6a-46b0-4735-85df-fd8c10ab46b8
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# shared_future::operator= Operator
Transfers an *associated asynchronous state* from a specified object.  
  
## Syntax  
  
```  
shared_future& operator=(shared_future&& Right) noexcept;  
shared_future& operator=(const shared_future& Right);  
```  
  
#### Parameters  
 `Right`  
 A `shared_future` object.  
  
## Return Value  
 `*this`  
  
## Remarks  
 For the first operator, `Right` no longer has an associated asynchronous state after the operation.  
  
 For the second method, `Right` maintains its associated asynchronous state.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [shared_future Class](../vs140/shared_future-Class.md)   
 [<future\>](../vs140/-future-.md)