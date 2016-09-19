---
title: "mutex::~mutex Destructor (STL)"
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
ms.assetid: bb0ab93d-72ba-4b9f-8272-86557e7f31e4
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# mutex::~mutex Destructor (STL)
Releases any resources that are used by the `mutex` object.  
  
## Syntax  
  
```cpp  
~mutex();  
```  
  
## Remarks  
 If the object is locked when the destructor runs, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)   
 [mutex Class (STL)](../vs140/mutex-Class--STL-.md)