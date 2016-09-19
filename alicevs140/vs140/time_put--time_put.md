---
title: "time_put::time_put"
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
ms.assetid: da0bd945-09db-4e2b-90eb-6e8e660b32b1
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# time_put::time_put
Constructor for objects of type `time_put`.  
  
## Syntax  
  
```  
explicit time_put(  
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
  
 The constructor initializes its base object with **locale::**[facet](../vs140/facet-Class.md)(**_***Refs*).  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [time_put Class](../vs140/time_put-Class.md)