---
title: "money_put::money_put"
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
ms.assetid: 1ec9db51-bc4c-463c-b83f-c00039771c47
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# money_put::money_put
The constructor for objects of type `money_put`.  
  
## Syntax  
  
```  
  
      explicit money  
      _  
      put(  
   size_t _Refs = 0  
);  
```  
  
#### Parameters  
 `_Refs`  
 Integer value used to specify the type of memory management for the object.  
  
## Remarks  
 The possible values for the `_Refs` parameter and their significance are:  
  
-   0: the lifetime of the object is managed by the locales that contain it.  
  
-   1: the lifetime of the object must be manually managed.  
  
-   \> 0: these values are not defined.  
  
 No direct examples are possible, because the destructor is protected.  
  
 The constructor initializes its base object with **locale::**[facet](../vs140/facet-Class.md)(`_Refs`).  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [money_put Class](../vs140/money_put-Class.md)