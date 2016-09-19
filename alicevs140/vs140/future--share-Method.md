---
title: "future::share Method"
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
ms.assetid: 285fb25a-00f9-4cd9-b40e-dcdc31628b9d
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# future::share Method
Converts the object to a [shared_future](../vs140/shared_future-Class.md) object.  
  
## Syntax  
  
```  
shared_future<Ty> share();  
```  
  
## Return Value  
 `shared_future(move(*this))`  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [future Class](../vs140/future-Class.md)   
 [<future\>](../vs140/-future-.md)   
 [move](../vs140/move.md)