---
title: "raw_native_types"
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
ms.assetid: 9f38daa8-8dc0-46a5-aff9-f1ff9c1e6f48
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# raw_native_types
**C++ Specific**  
  
 Disables the use of COM support classes in the high-level wrapper functions and forces the use of low-level data types instead.  
  
## Syntax  
  
```  
raw_native_types  
```  
  
## Remarks  
 By default, the high-level error-handling methods use the COM support classes [_bstr_t](../vs140/_bstr_t-Class.md) and [_variant_t](../vs140/_variant_t-Class.md) in place of the `BSTR` and **VARIANT** data types and raw COM interface pointers. These classes encapsulate the details of allocating and deallocating memory storage for these data types, and greatly simplify type casting and conversion operations.  
  
 **END C++ Specific**  
  
## See Also  
 [#import Attributes](../vs140/#import-Attributes--C---.md)   
 [The #import Directive](../vs140/#import-Directive--C---.md)