---
title: "num_put::num_put"
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
ms.assetid: 22ffc8e3-7217-4682-b5a0-4c28b8d0999a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# num_put::num_put
The constructor for objects of type `num_put`.  
  
## Syntax  
  
```  
explicit num_put(  
    size_t _Refs = 0  
);  
```  
  
#### Parameters  
 `_Refs`  
 Integer value used to specify the type of memory management for the object.  
  
## Remarks  
 The possible values for the `_Refs` parameter and their significance are:  
  
-   0: The lifetime of the object is managed by the locales that contain it.  
  
-   1: The lifetime of the object must be manually managed.  
  
-   \> 0: These values are not defined.  
  
 No direct examples are possible, because the destructor is protected.  
  
 The constructor initializes its base object with **locale::**[facet](../vs140/facet-Class.md)(_*Refs*).  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [num_put Class](../vs140/num_put-Class.md)