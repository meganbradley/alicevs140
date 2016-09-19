---
title: "Assertion and User-Supplied Messages (C++)"
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
ms.assetid: ebf7d885-61c8-4233-b0ae-1c9a38e0f385
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Assertion and User-Supplied Messages (C++)
The C++ language supports three error handling mechanisms that help you debug your application: the [#error directive](../vs140/#error-Directive--C-C---.md), the [static_assert](../vs140/static_assert.md) keyword, and the [assert (CRT)](../vs140/assert-Macro--_assert--_wassert.md) macro. All three mechanisms issue error messages, and two also test software assertions. A software assertion specifies a condition that you expect to be true at a particular point in your program. If a compile time assertion fails, the compiler issues a diagnostic message and a compilation error. If a run-time assertion fails, the operating system issues a diagnostic message and closes your application.  
  
## Remarks  
 The lifetime of your application consists of a preprocessing, compile, and run time phase. Each error handling mechanism accesses debug information that is available during one of these phases. To debug effectively, select the mechanism that provides appropriate information about that phase:  
  
-   The [#error directive](../vs140/#error-Directive--C-C---.md) is in effect at preprocessing time. It unconditionally emits a user-specified message and causes the compilation to fail with an error. The message can contain text that is manipulated by preprocessor directives but any resulting expression is not evaluated.  
  
-   The [static_assert](../vs140/static_assert.md) declaration is in effect at compile time. It tests a software assertion that is represented by a user-specified integral expression that can be converted to a Boolean. If the expression evaluates to zero (false), the compiler issues the user-specified message and the compilation fails with an error.  
  
     The `static_assert` declaration is especially useful for debugging templates because template arguments can be included in the user-specified expression.  
  
-   The [assert (CRT)](../vs140/assert-Macro--_assert--_wassert.md) macro is in effect at run time. It evaluates a user-specified expression, and if the result is zero, the system issues a diagnostic message and closes your application. Many other macros, such as[_ASSERT](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) and `_ASSERTE`, resemble this macro but issue different system-defined or user-defined diagnostic messages.  
  
## See Also  
 [The #error Directive](../vs140/#error-Directive--C-C---.md)   
 [assert (CRT)](../vs140/assert-Macro--_assert--_wassert.md)   
 [_ASSERT, _ASSERTE Macros](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md)   
 [static_assert](../vs140/static_assert.md)   
 [_STATIC_ASSERT Macro](../vs140/_STATIC_ASSERT-Macro.md)   
 [Templates](../vs140/Templates--C---.md)