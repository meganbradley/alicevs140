---
title: "shared_future::shared_future Constructor"
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
ms.assetid: 662abb26-27f9-400c-9628-ddfedf8b225c
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# shared_future::shared_future Constructor
Constructs a `shared_future` object.  
  
## Syntax  
  
```  
shared_future() _NOEXCEPT;  
shared_future(future<Ty>&& Right) _NOEXCEPT;  
shared_future(shared_future&& Right) _NOEXCEPT;  
shared_future(const shared_future& Right);  
```  
  
#### Parameters  
 `Right`  
 A [future](../vs140/future-Class.md) or `shared_future` object.  
  
## Remarks  
 The first constructor constructs a `shared_future` object that has no *associated asynchronous state*.  
  
 The second and third constructors construct a `shared_future` object and transfer the associated asynchronous state from `Right`. `Right` no longer has an associated asynchronous state.  
  
 The fourth constructor constructs a `shared_future` object that has the same associated asynchronous state as `Right`.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [shared_future Class](../vs140/shared_future-Class.md)   
 [<future\>](../vs140/-future-.md)