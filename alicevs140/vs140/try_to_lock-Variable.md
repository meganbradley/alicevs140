---
title: "try_to_lock Variable"
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
ms.assetid: 3126b9d6-9b09-4410-8a44-4098ea801d1b
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# try_to_lock Variable
Represents an object that can be passed to the constructor for [unique_lock](../vs140/unique_lock-Class.md) to indicate that the constructor should try to unlock the `mutex` that is also being passed to it without blocking.  
  
## Syntax  
  
```cpp  
const try_to_lock_t try_to_lock;  
```  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)