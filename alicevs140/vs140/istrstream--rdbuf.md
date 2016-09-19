---
title: "istrstream::rdbuf"
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
ms.assetid: 2a7f2b31-7c21-45da-8851-83ca02da9846
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# istrstream::rdbuf
Returns a pointer to the stream's associated strstreambuf object.  
  
## Syntax  
  
```  
  
strstreambuf *rdbuf( ) const  
  
```  
  
## Return Value  
 A pointer to the stream's associated strstreambuf object.  
  
## Remarks  
 The member function returns the address of the stored stream buffer, of type pointer to [strstreambuf](../vs140/strstreambuf-Class.md).  
  
## Example  
 See [strstreambuf::pcount](../vs140/strstreambuf--pcount.md) for a sample that uses `rdbuf`.  
  
## Requirements  
 **Header:** <strstream\>  
  
 **Namespace:** std  
  
## See Also  
 [istrstream Class](../vs140/istrstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)