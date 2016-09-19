---
title: "operator&lt;&lt; Operator (&lt;thread&gt;)"
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
ms.assetid: 705d8280-1379-445d-b924-3fec0cd1dbd7
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt;&lt; Operator (&lt;thread&gt;)
Inserts a text representation of a `thread::id` object into a stream.  
  
## Syntax  
  
```cpp  
template<class Elem, class Tr>  
   basic_ostream<Elem, Tr>& operator<<(  
      basic_ostream<Elem, Tr>& Ostr, thread::id Id);  
```  
  
#### Parameters  
 `Ostr`  
 A [basic_ostream](../vs140/basic_ostream-Class.md) object.  
  
 `Id`  
 A `thread::id` object.  
  
## Return Value  
 `Ostr`.  
  
## Remarks  
 This function inserts `Id` into `Ostr`.  
  
 If two `thread::id` objects compare equal, the inserted text representations of those objects are the same.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<thread\>](../vs140/-thread-.md)