---
title: "raw_method_prefix"
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
ms.assetid: 71490313-af78-4bb2-b28a-eee67950d30b
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# raw_method_prefix
**C++ Specific**  
  
 Specifies a different prefix to avoid name collisions.  
  
## Syntax  
  
```  
raw_method_prefix("Prefix")  
```  
  
#### Parameters  
 `Prefix`  
 The prefix to be used.  
  
## Remarks  
 Low-level properties and methods are exposed by member functions named with a default prefix of **raw_** to avoid name collisions with the high-level error-handling member functions.  
  
> [!NOTE]
>  The effects of the `raw_method_prefix` attribute will not be changed by the presence of the [raw_interfaces_only](#_predir_raw_interfaces_only) attribute. The `raw_method_prefix` always takes precedence over `raw_interfaces_only` in specifying a prefix. If both attributes are used in the same `#import` statement, then the prefix specified by the `raw_method_prefix` attribute is used.  
  
 **END C++ Specific**  
  
## See Also  
 [#import Attributes](../vs140/#import-Attributes--C---.md)   
 [The #import Directive](../vs140/#import-Directive--C---.md)