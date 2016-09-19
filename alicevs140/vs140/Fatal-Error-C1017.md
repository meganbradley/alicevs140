---
title: "Fatal Error C1017"
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
ms.topic: error-reference
ms.assetid: 5542e604-599d-4e36-8f83-1d454c5753c9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1017
invalid integer constant expression  
  
 The expression in an `#if` directive did not exist or did not evaluate to a constant.  
  
 Constants defined using `#define` must have values that evaluate to an integer constant if they are used in an `#if`, `#elif`, or `#else` directive.  
  
 The following sample generates C1017:  
  
```  
// C1017.cpp  
#define CONSTANT_NAME "YES"  
#if CONSTANT_NAME   // C1017  
#endif  
```  
  
 Possible resolution:  
  
```  
// C1017b.cpp  
// compile with: /c  
#define CONSTANT_NAME 1  
#if CONSTANT_NAME  
#endif  
```  
  
 Because `CONSTANT_NAME` evaluates to a string and not an integer, the `#if` directive generates fatal error C1017.  
  
 In other cases, the preprocessor evaluates an undefined constant as zero. This can cause unintended results, as shown in the following sample. `YES` is undefined, so it evaluates to zero. The expression `#if` `CONSTANT_NAME` evaluates to false and the code to be used on `YES` is removed by the preprocessor. `NO` is also undefined (zero), so `#elif` `CONSTANT_NAME==NO` evaluates to true (`0 == 0`), causing the preprocessor to leave the code in the `#elif` portion of the statement — exactly the opposite of the intended behavior.  
  
```  
// C1017c.cpp  
// compile with: /c  
#define CONSTANT_NAME YES  
#if CONSTANT_NAME  
   // Code to use on YES...  
#elif CONSTANT_NAME==NO  
   // Code to use on NO...  
#endif  
```  
  
 To see exactly how the compiler handles preprocessor directives, use [/P](../vs140/-P--Preprocess-to-a-File-.md), [/E](../vs140/-E--Preprocess-to-stdout-.md), or [/EP](../vs140/-EP--Preprocess-to-stdout-Without-#line-Directives-.md).