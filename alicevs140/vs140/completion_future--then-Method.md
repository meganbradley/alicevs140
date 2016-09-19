---
title: "completion_future::then Method"
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
ms.assetid: b0193808-be8a-4785-ba9e-e4d46329aaac
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# completion_future::then Method
Chains a callback function object to the `completion_future` object to be executed when the associated asynchronous operation finishes execution.  
  
## Syntax  
  
```  
template <  
   typename _Functor  
>  
void then(  
   const _Functor &_Func  
) const;  
```  
  
#### Parameters  
 `_Functor`  
 The callback functor.  
  
 `_Func`  
 The callback function object.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [completion_future Class](../vs140/completion_future-Class.md)