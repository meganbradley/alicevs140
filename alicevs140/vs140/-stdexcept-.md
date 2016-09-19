---
title: "&lt;stdexcept&gt;"
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
ms.assetid: 495c10b1-1e60-4514-9f8f-7fda11a2f522
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;stdexcept&gt;
Defines several standard classes used for reporting exceptions. The classes form a derivation hierarchy all derived from class [exception](../vs140/exception-Class.md) and include two general types of exceptions: logical errors and run-time errors. The logical errors are caused programmer mistakes. They derive from the base class logic_error and include:  
  
-   `domain_error`  
  
-   `invalid_argument`  
  
-   `length_error`  
  
-   `out_of_range`  
  
 The run-time errors occur because of mistakes in either the library functions or in the run-time system. They derive from the base class runtime_error and include:  
  
-   `overflow_error`  
  
-   `range_error`  
  
-   `underflow_error`  
  
### Classes  
  
|||  
|-|-|  
|[domain_error Class](../vs140/domain_error-Class.md)|The class serves as the base class for all exceptions thrown to report a domain error.|  
|[invalid_argument Class](../vs140/invalid_argument-Class.md)|The class serves as the base class for all exceptions thrown to report an invalid argument.|  
|[length_error Class](../vs140/length_error-Class.md)|The class serves as the base class for all exceptions thrown to report an attempt to generate an object too long to be specified.|  
|[logic_error Class](../vs140/logic_error-Class.md)|The class serves as the base class for all exceptions thrown to report errors presumably detectable before the program executes, such as violations of logical preconditions.|  
|[out_of_range Class](../vs140/out_of_range-Class.md)|The class serves as the base class for all exceptions thrown to report an argument that is out of its valid range.|  
|[overflow_error Class](../vs140/overflow_error-Class.md)|The class serves as the base class for all exceptions thrown to report an arithmetic overflow.|  
|[range_error Class](../vs140/range_error-Class.md)|The class serves as the base class for all exceptions thrown to report a range error.|  
|[runtime_error Class](../vs140/runtime_error-Class.md)|The class serves as the base class for all exceptions thrown to report errors presumably detectable only when the program executes.|  
|[underflow_error Class](../vs140/underflow_error-Class.md)|The class serves as the base class for all exceptions thrown to report an arithmetic underflow.|  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)