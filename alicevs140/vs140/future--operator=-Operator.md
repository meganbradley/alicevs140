---
title: "future::operator= Operator"
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
ms.assetid: a4e49a7c-0f0a-4905-b14f-e5437637d3b2
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# future::operator= Operator
Transfers an associated asynchronous state from a specified object.  
  
## Syntax  
  
```  
future& operator=(  
   future&& Right  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Right`  
 A `future` object.  
  
## Return Value  
 `*this`  
  
## Remarks  
 After the transfer, `Right` no longer has an associated asynchronous state.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [future Class](../vs140/future-Class.md)   
 [<future\>](../vs140/-future-.md)