---
title: "Preprocessor Directives"
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
ms.assetid: e0fc4564-b6cf-4a36-bf51-6ccd7abd0a94
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Preprocessor Directives
Preprocessor directives, such as `#define` and **#ifdef**, are typically used to make source programs easy to change and easy to compile in different execution environments. Directives in the source file tell the preprocessor to perform specific actions. For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text. Preprocessor lines are recognized and carried out before macro expansion. Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.  
  
 Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported. The character set used in preprocessor statements is the same as the [execution character set](assetId:///a7901c61-524d-47c6-beb6-d9dacc2e72ed). The preprocessor also recognizes negative character values.  
  
 The preprocessor recognizes the following directives:  
  
|||||  
|-|-|-|-|  
|[#define](../vs140/#define-Directive--C-C---.md)|[#error](../vs140/#error-Directive--C-C---.md)|[#import](../vs140/#import-Directive--C---.md)|[#undef](../vs140/#undef-Directive--C-C---.md)|  
|[#elif](../vs140/#if--#elif--#else--and-#endif-Directives--C-C---.md)|[#if](../vs140/#if--#elif--#else--and-#endif-Directives--C-C---.md)|[#include](../vs140/#include-Directive--C-C---.md)|[#using](../vs140/#using-Directive--C---.md)|  
|[#else](../vs140/#if--#elif--#else--and-#endif-Directives--C-C---.md)|[#ifdef](../vs140/#ifdef-and-#ifndef-Directives--C-C---.md)|[#line](../vs140/#line-Directive--C-C---.md)|[#endif](../vs140/#if--#elif--#else--and-#endif-Directives--C-C---.md)|  
|[#ifndef](../vs140/#ifdef-and-#ifndef-Directives--C-C---.md)|[#pragma](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)|||  
  
 The number sign (**#**) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive. Some directives include arguments or values. Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (**//**) or enclosed in comment delimiters (**/\* \*/**). Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (**\\**).  
  
 Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.  
  
## See Also  
 [Preprocessor Operators](../vs140/Preprocessor-Operators.md)   
 [Predefined Macros](../vs140/Predefined-Macros.md)   
 [C/C++ Preprocessor Reference](../vs140/C-C---Preprocessor-Reference.md)