---
title: "ios_base::iostate"
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
ms.assetid: 09b5849e-3ab8-4829-aecc-82f799bb9370
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::iostate
The type of constants that describe the state of a stream.  
  
## Syntax  
  
```  
namespace std {  
   class ios_base {  
   public:  
      typedef implementation-defined-bitmask-type iostate;  
      static const iostate badbit;  
      static const iostate eofbit;  
      static const iostate failbit;  
      static const iostate goodbit;  
      ...  
   };  
}  
```  
  
## Remarks  
 The type is a bitmask type that describes an object that can store stream state information. The distinct flag values (elements) are:  
  
-   `badbit`, to record a loss of integrity of the stream buffer.  
  
-   `eofbit`, to record end-of-file while extracting from a stream.  
  
-   `failbit`, to record a failure to extract a valid field from a stream.  
  
 In addition, a useful value is `goodbit`, where none of the previously mentioned bits are set (`goodbit` is guaranteed to be zero).  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)