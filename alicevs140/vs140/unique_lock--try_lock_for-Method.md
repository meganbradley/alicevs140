---
title: "unique_lock::try_lock_for Method"
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
ms.assetid: f33be1a9-eb08-4d29-ad5b-4b081f413c04
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unique_lock::try_lock_for Method
Attempts to obtain ownership of the associated `mutex` without blocking.  
  
## Syntax  
  
```  
template<class Rep,  
   class Period>  
bool try_lock_for(  
   const chrono::duration<Rep,  
   Period>& Rel_time  
);  
```  
  
#### Parameters  
 `Rel_time`  
 A [chrono::duration](../vs140/duration-Class.md) object that specifies the maximum amount of time that the method attempts to obtain ownership of the `mutex`.  
  
## Return Value  
 `true` if the method successfully obtains ownership of the `mutex`; otherwise, `false`.  
  
## Remarks  
 If the stored `mutex` pointer is `null`, the method throws a [system_error](../vs140/system_error-Class.md) that has an error code of `operation_not_permitted`.  
  
 If the calling thread already owns the `mutex`, the method throws a `system_error` that has an error code of `resource_deadlock_would_occur`.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [unique_lock Class](../vs140/unique_lock-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)