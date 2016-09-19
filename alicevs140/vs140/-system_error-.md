---
title: "&lt;system_error&gt;"
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
ms.assetid: 5e046c6e-48d9-4740-8c8a-05f3727c1215
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;system_error&gt;
Include the header `<system_error>` to define the exception class `system_error` and related templates for processing low-level system errors.  
  
## Syntax  
  
```  
#include <system_error>  
```  
  
### Objects  
  
|||  
|-|-|  
|[generic_category](../vs140/-system_error--functions.md#generic_category)|Represents the category for generic errors.|  
|[system_category](../vs140/-system_error--functions.md#system_category)|Represents the category for errors caused by low-level system overflows.|  
  
### Typedefs  
  
|||  
|-|-|  
|[generic_errno](../vs140/-system_error--typedefs.md#generic_errno)|A type that represents the enumeration that provides the symbolic names for all the error-code macros defined by Posix in `<errno.h>`.|  
  
### Functions  
  
|||  
|-|-|  
|[make_error_code](../vs140/-system_error--functions.md#make_error_code)|Creates an `error_code` object.|  
|[make_error_condition](../vs140/-system_error--functions.md#make_error_condition)|Creates an `error_condition` object.|  
  
### Operators  
  
|||  
|-|-|  
|[operator==](../vs140/-system_error--operators.md#operator_eq_eq)|Tests if the object on the left side of the operator is equal to the object on the right side.|  
|[operator!=](../vs140/-system_error--operators.md#operator_neq)|Tests if the object on the left side of the operator is not equal to the object on the right side.|  
|[operator<](../vs140/-system_error--operators.md#operator_lt_)|Tests if an object is less than the object passed in for comparison.|  
  
### Enumerations  
  
|||  
|-|-|  
|[errc](../vs140/-system_error--enums.md#errc_enumeration)|Provides symbolic names for all the error-code macros defined by Posix in `<errno.h>`.|  
  
### Classes and Structs  
  
|||  
|-|-|  
|[error_category](../vs140/error_category-Class.md)|Represents the abstract, common base for objects that describes a category of error codes.|  
|[error_code](../vs140/error_code-Class.md)|Represents low-level system errors that are implementation-specific.|  
|[error_condition](../vs140/error_condition-Class.md)|Represents user-defined error codes.|  
|[is_error_code_enum](../vs140/is_error_code_enum-Class.md)|Represents a type predicate that tests for the [error_code](../vs140/error_code-Class.md) enumeration.|  
|[is_error_condition_enum](../vs140/is_error_condition_enum-Class.md)|Represents a type predicate that tests for the [error_condition](../vs140/error_condition-Class.md) enumeration.|  
|[system_error](../vs140/system_error-Class.md)|Represents the base class for all exceptions thrown to report a low-level system overflow.|  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)