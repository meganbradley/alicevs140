---
title: "future::future Constructor"
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
ms.assetid: dcb3422a-7566-4a58-8b16-a7606e5808f1
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# future::future Constructor
Constructs a `future` object.  
  
## Syntax  
  
```  
future() _NOEXCEPT;  
future(  
   future&& Other  
) _NOEXCEPT;  
  
```  
  
#### Parameters  
 `Other`  
 A `future` object.  
  
## Remarks  
 The first constructor constructs a `future` object that has no associated asynchronous state.  
  
 The second constructor constructs a `future` object and transfers the associated asynchronous state from `Other`. `Other` no longer has an associated asynchronous state.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [future Class](../vs140/future-Class.md)   
 [<future\>](../vs140/-future-.md)