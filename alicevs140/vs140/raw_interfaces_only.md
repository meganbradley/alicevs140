---
title: "raw_interfaces_only"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 87056c6d-3f34-4248-af58-f5775a35bfb7
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# raw_interfaces_only
**C++ Specific**  
  
 Suppresses the generation of error-handling wrapper functions and [property](../vs140/property--C---.md) declarations that use those wrapper functions.  
  
## Syntax  
  
```  
raw_interfaces_only  
```  
  
## Remarks  
 The `raw_interfaces_only` attribute also causes the default prefix used in naming the non-property functions to be removed. Normally, the prefix is **raw_**. If this attribute is specified, the function names are directly from the type library.  
  
 This attribute allows you to expose only the low-level contents of the type library.  
  
 **END C++ Specific**  
  
## See Also  
 [#import Attributes](../vs140/#import-Attributes--C---.md)   
 [The #import Directive](../vs140/#import-Directive--C---.md)