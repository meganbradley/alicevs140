---
title: "timed_mutex::~timed_mutex Destructor"
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
ms.assetid: d853d9af-b1c0-4402-a9ce-a579ba5a6fc5
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# timed_mutex::~timed_mutex Destructor
Releases any resources that are used by the `mutex` object.  
  
## Syntax  
  
```cpp  
~timed_mutex();  
```  
  
## Remarks  
 If the object is locked when the destructor runs, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)   
 [timed_mutex Class](../vs140/timed_mutex-Class.md)