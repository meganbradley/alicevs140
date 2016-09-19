---
title: "codecvt::codecvt"
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
ms.assetid: 70f64142-b925-4bbb-aa6d-697e7168ecae
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# codecvt::codecvt
The constructor for objects of class codecvt that serves as a locale facet to handle conversions.  
  
## Syntax  
  
```  
explicit codecvt(  
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
  
 The constructor initializes its `locale::facet` base object with **locale::**[facet](../vs140/facet-Class.md)(`_Refs`)*.*  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [codecvt Class](../vs140/codecvt-Class.md)