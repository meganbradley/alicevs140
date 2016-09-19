---
title: "recursive_mutex::~recursive_mutex Destructor"
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
ms.assetid: 31942832-1cf8-4184-8ea5-d2694cb8f8ef
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# recursive_mutex::~recursive_mutex Destructor
Releases any resources that are used by the object.  
  
## Syntax  
  
```cpp  
~recursive_mutex();  
```  
  
## Remarks  
 If the object is locked when the destructor runs, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [recursive_mutex Class](../vs140/recursive_mutex-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)