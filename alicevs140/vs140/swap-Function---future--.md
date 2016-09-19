---
title: "swap Function (&lt;future&gt;)"
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
ms.assetid: c1f51935-9128-4376-b487-d9c3b37b6819
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap Function (&lt;future&gt;)
Exchanges the *associated asynchronous state* of one `promise` object with that of another.  
  
## Syntax  
  
```  
template<class Ty>  
   void swap(promise<Ty>& Left, promise<Ty>& Right) noexcept;  
template<class Ty, class... ArgTypes>  
   void swap(packaged_task<Ty(ArgTypes...)>& Left,  
      packaged_task<Ty(ArgTypes...)>& Right) noexcept;  
```  
  
#### Parameters  
 `Left`  
 The left `promise` object.  
  
 `Right`  
 The right `promise` object.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [promise Class](../vs140/promise-Class.md)   
 [<future\>](../vs140/-future-.md)