---
title: "operator&gt;= Operator (&lt;thread&gt;)"
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
ms.assetid: 3e2c5c5b-46ca-41c3-8db7-c2302adcdca0
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&gt;= Operator (&lt;thread&gt;)
Determines whether one `thread::id` object is greater than or equal to another.  
  
## Syntax  
  
```cpp  
bool operator>= (  
   thread::id Left,  
   thread::id Right) _NOEXCEPT  
```  
  
#### Parameters  
 `Left`  
 The left `thread::id` object.  
  
 `Right`  
 The right `thread::id` object.  
  
## Return Value  
 `!(Left < Right)`  
  
## Remarks  
 This function does not throw any exceptions.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<thread\>](../vs140/-thread-.md)   
 [operator< Operator (<thread\>)](../vs140/operator--Operator---thread--.md)