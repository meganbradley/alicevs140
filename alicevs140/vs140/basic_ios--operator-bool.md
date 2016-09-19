---
title: "basic_ios::operator bool"
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
ms.assetid: b0fd4c14-326c-47e8-a785-52218f09173e
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_ios::operator bool
Allows use of a `basic_ios` object as a `bool`. Automatic type conversion is disabled to prevent common, unintended side effects.  
  
## Syntax  
  
```  
explicit operator bool() const;  
```  
  
## Remarks  
 The operator returns a value convertible to `false` only if `fail``()`. The return type is convertible only to `bool`, not to `void *` or other known scalar type.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)