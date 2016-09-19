---
title: "strstreambuf::underflow"
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
ms.assetid: 16d40405-4d47-4055-909a-f0c668b26542
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strstreambuf::underflow
A protected virtual function to extract the current element from the input stream.  
  
## Syntax  
  
```  
  
virtual int underflow( );  
  
```  
  
## Return Value  
 If the function cannot succeed, it returns `EOF`. Otherwise, it returns the current element in the input stream, converted as described above.  
  
## Remarks  
 The protected virtual member function endeavors to extract the current element **ch** from the input buffer, then advance the current stream position, and return the element as (`int`)(`unsigned` `char`)**ch**. It can do so in only one way: if a read position is available, it takes **ch** as the element stored in the read position and advances the next pointer for the input buffer.  
  
## Requirements  
 **Header:** <strstream\>  
  
 **Namespace:** std  
  
## See Also  
 [strstreambuf Class](../vs140/strstreambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)