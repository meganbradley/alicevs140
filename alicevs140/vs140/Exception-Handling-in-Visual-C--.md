---
title: "Exception Handling in Visual C++"
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
ms.topic: language-reference
ms.assetid: a6aa08de-669d-4ce8-9ec3-ec20d1354fcf
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exception Handling in Visual C++
An exception is an error condition, possibly outside the program's control, that prevents the program from continuing along its regular execution path. Certain operations, including object creation, file input/output, and function calls made from other modules, are all potential sources of exceptions even when your program is running correctly. Robust code anticipates and handles exceptions.  
  
 To detect logic errors within a single program or module, use assertions rather than exceptions (see [Using Assertions](../vs140/C-C---Assertions.md)).  
  
 Visual C++ supports three kinds of exception handling:  
  
-   [C++ exception handling](../vs140/C---Exception-Handling.md)  
  
     For most C++ programs, you should use C++ exception handling, which is type-safe and ensures that object destructors are invoked during stack unwinding.  
  
-   [Structured exception handling](../vs140/Structured-Exception-Handling--C-C---.md)  
  
     Windows supplies its own exception mechanism, called SEH. It is not recommended for C++ or MFC programming. Use SEH only in non-MFC C programs.  
  
-   [MFC exceptions](../vs140/Exception-Handling-in-MFC.md)  
  
     Since version 3.0, MFC has used C++ exceptions but still supports its older exception handling macros, which are similar to C++ exceptions in form. Although these macros are not recommended for new programming, they are still supported for backward compatibility. In programs that already use the macros, you can freely use C++ exceptions as well. During preprocessing, the macros evaluate to the exception handling keywords defined in the Visual C++ implementation of the C++ language as of Visual C++ version 2.0. You can leave existing exception macros in place while you begin to use C++ exceptions.  
  
 Use the [/EH](../vs140/-EH--Exception-Handling-Model-.md) compiler option to specify the type of exception handling to use in a project; C++ exception handling is the default. Do not mix the error handling mechanisms; for example, do not use C++ exceptions with structured exception handling. Using C++ exception handling makes your code more portable, and it allows you to handle exceptions of any type. For more information about the drawbacks of structured exception handling, see [Structured Exception Handling](../vs140/Structured-Exception-Handling--C-C---.md). For advice about mixing MFC macros and C++ exceptions, see [Exceptions: Using MFC Macros and C++ Exceptions](../vs140/Exceptions--Using-MFC-Macros-and-C---Exceptions.md).  
  
 For information on handling exceptions in CLR applications, see [Exception Handling under /clr](../vs140/Exception-Handling---C---Component-Extensions-.md).  
  
 For information about exception handling on x64 processors, see [Exception Handling (x64)](../vs140/Exception-Handling--x64-.md).  
  
## See Also  
 [C++ Language Reference](../vs140/C---Language-Reference.md)