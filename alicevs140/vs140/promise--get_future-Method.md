---
title: "promise::get_future Method"
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
ms.assetid: ae5ca9f5-0934-4b75-bf23-a1cb86a42da7
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# promise::get_future Method
Returns a [future](../vs140/future-Class.md) object that has the same *associated asynchronous state* as this promise.  
  
## Syntax  
  
```  
future<Ty> get_future();  
```  
  
## Remarks  
 If the promise object is empty, this method throws a [future_error](../vs140/future_error-Class.md) that has an [error_code](../vs140/error_code-Class.md) of `no_state`.  
  
 If this method has already been called for a promise object that has the same associated asynchronous state, the method throws a `future_error` that has an `error_code` of `future_already_retrieved`.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [promise Class](../vs140/promise-Class.md)   
 [<future\>](../vs140/-future-.md)