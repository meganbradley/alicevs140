---
title: "ostrstream::freeze"
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
ms.assetid: 14157ccd-35c3-4f27-984f-330f06c0322a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostrstream::freeze
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
 The member function calls [rdbuf](../vs140/ostrstream--rdbuf.md) -> [freeze](../vs140/strstreambuf--freeze.md)(_*Freezeit*).  
  
## Example  
 See [strstream::freeze](../vs140/strstreambuf--freeze.md) for an example that uses **freeze**.  
  
## Requirements  
 **Header:** <strstream\>  
  
 **Namespace:** std  
  
## See Also  
 [ostrstream Class](../vs140/ostrstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)