---
title: "stdext Namespace"
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
ms.assetid: 3e94fc89-0584-424f-bc09-081b73379545
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# stdext Namespace
Members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are not currently part of the ISO C++ standard. Therefore, these types and members have been moved from the `std` namespace to namespace `stdext`, to remain conformant with the C++ standard.  
  
 When compiling with [/Ze](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md), which is the default, the compiler will warn on the use of `std` for members of the <hash_map> and <hash_set> header files. To disable the warning, use the [warning](../vs140/warning.md) pragma.  
  
 To have the compiler generate an error for the use of `std` for members of the <hash_map> and <hash_set> header files with **/Ze**, add the following directive before #include'ing any Standard C++ Library header files.  
  
```  
#define _DEFINE_DEPRECATED_HASH_CLASSES 0  
```  
  
 When compiling with **/Za**, the compiler will generate an error.  
  
## See Also  
 [Standard C++ Library Overview](../vs140/C---Standard-Library-Overview.md)