---
title: "strstreambuf::pbackfail"
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
ms.assetid: 1dc02c72-6c2f-4e66-a48e-f4c7a3b10720
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# strstreambuf::pbackfail
A protected virtual member function that tries to put back an element into the input stream, and then makes it the current element (pointed to by the next pointer).  
  
## Syntax  
  
```  
  
      virtual int pbackfail(  
   int _Meta = EOF  
);  
```  
  
#### Parameters  
 `_Meta`  
 The character to insert into the buffer, or `EOF`.  
  
## Return Value  
 If the function cannot succeed, it returns `EOF`. Otherwise, if _*Meta* == `EOF`, it returns some value other than `EOF`. Otherwise, it returns \_*Meta*.  
  
## Remarks  
 The protected virtual member function tries to put back an element into the input buffer, and then make it the current element (pointed to by the next pointer).  
  
 If _*Meta* == `EOF`, the element to push back is effectively the one already in the stream before the current element. Otherwise, that element is replaced by **ch** = (`char`)\_*Meta*. The function can put back an element in various ways:  
  
-   If a putback position is available, and the element stored there compares equal to **ch**, it can decrement the next pointer for the input buffer.  
  
-   If a putback position is available, and if the strstreambuf mode says the controlled sequence is modifiable, the function can store **ch** into the putback position and decrement the next pointer for the input buffer.  
  
## Requirements  
 **Header:** <strstream\>  
  
 **Namespace:** std  
  
## See Also  
 [strstreambuf Class](../vs140/strstreambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)