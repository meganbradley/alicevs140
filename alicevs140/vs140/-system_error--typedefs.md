---
title: "&lt;system_error&gt; typedefs"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 28cf9f7d-9c28-4baa-a297-67c8260b07fb
caps.latest.revision: 11
---
# &lt;system_error&gt; typedefs
||  
|-|  
|[generic_errno](#generic_errno)|  
  
##  <a name="generic_errno"></a>  generic_errno  
 A type that represents the enumeration that provides the symbolic names for all the error-code macros defined by Posix in `<errno.h>`.  
  
```  
typedef errc generic_error;  
```  
  
### Remarks  
 The type is a synonym for [errc](../vs140/-system_error--enums.md#errc_enumeration).  
  
## See Also  
 [&lt;system_error&gt;](../vs140/-system_error-.md)