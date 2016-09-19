---
title: "recursive_timed_mutex::~recursive_timed_mutex Destructor"
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
ms.assetid: 182d4f31-827b-4741-9130-6c9ad907d634
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# recursive_timed_mutex::~recursive_timed_mutex Destructor
Releases any resources that are used by the `recursive_timed_mutex` object.  
  
## Syntax  
  
```cpp  
~recursive_timed_mutex();  
```  
  
## Remarks  
 If the object is locked when the destructor runs, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)   
 [recursive_timed_mutex Class](../vs140/recursive_timed_mutex-Class.md)