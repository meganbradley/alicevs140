---
title: "nullptr"
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
ms.assetid: e9d80ea6-2506-4eb5-b47b-2349df085832
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# nullptr
Designates a null pointer constant of type `std::nullptr_t`, which is convertible to any raw pointer type.  Although you can use the keyword `nullptr` without including any headers, if your code uses the type `std::nullptr_t`, then you must define it by including the header `<cstddef>`.  
  
> [!NOTE]
>  The `nullptr` keyword is also defined in C++/CLI for managed code applications and is not interchangeable with the ISO Standard C++ keyword. If your code might be compiled by using the [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) compiler option, which targets managed code, then use `__nullptr` in any line of code where you must guarantee that the compiler uses the native C++ interpretation. For more information, see [nullptr (C++/CLI)](../vs140/nullptr---C---Component-Extensions-.md).  
  
## Remarks  
 Avoid using `NULL` or zero (`0`) as a null pointer constant; `nullptr` is less vulnerable to misuse and works better in most situations.  For example, given `func(std::pair<const char *, double>)`, then calling `func(std::make_pair(NULL, 3.14))` causes a compiler error.  The macro NULL expands to `0`, so that the call `std::make_pair(0, 3.14)` returns `std::pair<int, double>`, which is not convertible to func()'s `std::pair<const char *, double>` parameter type.  Calling `func(std::make_pair(nullptr, 3.14))` successfully compiles because `std::make_pair(nullptr, 3.14)` returns `std::pair<std::nullptr_t, double>`, which is convertible to `std::pair<const char *, double>`.  
  
## See Also  
 [Keywords](../vs140/Keywords--C---.md)   
 [nullptr (C++/CLI)](../vs140/nullptr---C---Component-Extensions-.md)