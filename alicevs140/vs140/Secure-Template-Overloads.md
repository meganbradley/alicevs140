---
title: "Secure Template Overloads"
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
ms.assetid: 562741d0-39c0-485e-8529-73d740f29f8f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Secure Template Overloads
Many CRT functions have been deprecated in favor of newer, security-enhanced versions (for example, `strcpy_s` is the more secure replacement for `strcpy`). The CRT provides template overloads to help ease the transition to the more secure variants.  
  
 For example, this code generates a warning because `strcpy` is deprecated:  
  
 `char szBuf[10];`  
  
 `strcpy(szBuf, "test"); // warning: deprecated`  
  
 You can ignore the warning. Define the symbol `_CRT_SECURE_NO_WARNINGS` to suppress the warning, or update the code to use `strcpy_s`:  
  
 `char szBuf[10];`  
  
 `strcpy_s(szBuf, 10, "test"); // security-enhanced _s function`  
  
 The template overloads provide additional choices. Defining `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES` to 1 enables template overloads of standard CRT functions that call the more secure variants automatically. If `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES` is 1, then no changes to the code are necessary. Behind the scenes, the call to `strcpy` will be changed to a call to `strcpy_s` with the size argument supplied automatically.  
  
 `#define _CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES 1`  
  
 `...`  
  
 `char szBuf[10];`  
  
 `strcpy(szBuf, "test"); // ==> strcpy_s(szBuf, 10, "test")`  
  
 `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES` does not affect the functions that take a count, such as `strncpy`. To enable template overloads for the count functions, define `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES_COUNT` to 1. Before doing so, however, make sure that your code passes the count of characters, not the size of the buffer (a common mistake). Also, code that explicitly writes a null terminator at the end of the buffer after the function call is unnecessary if the secure variant is called. If you need truncation behavior, see [_TRUNCATE](../vs140/_TRUNCATE.md).  
  
> [!NOTE]
>  The macro `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES_COUNT` requires that `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES` is also defined as 1. If `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES_COUNT` is defined as 1 and `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES` is defined as 0, the application will not perform any template overloads.  
  
 Defining `_CRT_SECURE_CPP_OVERLOAD_SECURE_NAMES` to 1 enables template overloads of the secure variants (names ending in "_s"). In this case, if `_CRT_SECURE_CPP_OVERLOAD_SECURE_NAMES` is 1, then one small change must be made to the original code:  
  
 `#define _CRT_SECURE_CPP_OVERLOAD_SECURE_NAMES 1`  
  
 `...`  
  
 `char szBuf[10];`  
  
 `strcpy_s(szBuf, "test"); // ==> strcpy_s(szBuf, 10, "test")`  
  
 Only the name of the function needs to be changed (by adding "_s"); the template overload will take care of providing the size argument.  
  
 By default, `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES` and `_CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES_COUNT` are defined as 0 (disabled) and `_CRT_SECURE_CPP_OVERLOAD_SECURE_NAMES` is defined as 1 (enabled).  
  
 Note that these template overloads only work for static arrays. Dynamically allocated buffers require additional source code changes. Revisiting the above examples:  
  
 `#define _CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES 1`  
  
 `...`  
  
 `char *szBuf = (char*)malloc(10);`  
  
 `strcpy(szBuf, "test"); // still deprecated; have to change to`  
  
 `// strcpy_s(szBuf, 10, "test");`  
  
 And this:  
  
 `#define _CRT_SECURE_CPP_OVERLOAD_SECURE_NAMES 1`  
  
 `...`  
  
 `char *szBuf = (char*)malloc(10);`  
  
 `strcpy_s(szBuf, "test"); // doesn't compile; have to change to`  
  
 `// strcpy_s(szBuf, 10, "test");`  
  
## See Also  
 [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md)   
 [CRT Library Features](../vs140/CRT-Library-Features.md)