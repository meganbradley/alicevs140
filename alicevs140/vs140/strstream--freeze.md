---
title: "strstream::freeze"
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
ms.assetid: 29b5bf14-7d08-4790-b7cd-dbced1e9c13e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strstream::freeze
Causes a stream buffer to be unavailable through stream buffer operations.  
  
## Syntax  
  
```  
  
      void freeze(  
   bool _Freezeit = true  
);  
```  
  
#### Parameters  
 `_Freezeit`  
 A `bool` indicating whether you want the stream to be frozen.  
  
## Remarks  
 The member function calls [rdbuf](../vs140/strstream--rdbuf.md) -> [freeze](../vs140/strstreambuf--freeze.md)(_*Freezeit*).  
  
## Example  
 See [strstreambuf::freeze](../vs140/strstreambuf--freeze.md) for an example that uses **freeze**.  
  
## Requirements  
 **Header:** <strstream\>  
  
 **Namespace:** std  
  
## See Also  
 [strstream Class](../vs140/strstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)