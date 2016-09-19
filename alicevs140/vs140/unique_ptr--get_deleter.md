---
title: "unique_ptr::get_deleter"
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
ms.assetid: e0fcb3c2-fd8e-44f1-be4b-c5310907570e
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unique_ptr::get_deleter
Returns a reference to `stored_deleter`.  
  
## Syntax  
  
```  
Del& get_deleter();  
const Del& get_deleter() const;  
```  
  
## Property Value/Return Value  
 Returns a reference to `stored_deleter`.  
  
## Remarks  
 The member function returns a reference to `stored_deleter`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [unique_ptr](../vs140/unique_ptr-Class.md)   
 [<memory\>](../vs140/-memory-.md)