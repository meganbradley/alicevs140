---
title: "Preprocessor"
ms.custom: na
ms.date: 09/18/2016
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
ms.assetid: e120eda3-b413-49f1-a07c-e9fb128cf500
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Preprocessor
The preprocessor is a text processor that manipulates the text of a source file as part of the first phase of translation. The preprocessor does not parse the source text, but it does break it up into tokens for the purpose of locating macro calls. Although the compiler ordinarily invokes the preprocessor in its first pass, the preprocessor can also be invoked separately to process text without compiling.  
  
 The reference material on the preprocessor includes the following sections:  
  
-   [Preprocessor directives](../vs140/Preprocessor-Directives.md)  
  
-   [Preprocessor operators](../vs140/Preprocessor-Operators.md)  
  
-   [Predefined macros](../vs140/Predefined-Macros.md)  
  
-   [Pragmas](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)  
  
 **Microsoft Specific**  
  
 You can obtain a listing of your source code after preprocessing by using the [/E](../vs140/-E--Preprocess-to-stdout-.md) or [/EP](../vs140/-EP--Preprocess-to-stdout-Without-#line-Directives-.md) compiler option. Both options invoke the preprocessor and output the resulting text to the standard output device, which, in most cases, is the console. The difference between the two options is that /E includes `#line` directives and /EP strips these directives out.  
  
 **END Microsoft Specific**  
  
##  <a name="_predir_special_terminology"></a> Special Terminology  
 In the preprocessor documentation, the term "argument" refers to the entity that is passed to a function. In some cases, it is modified by "actual" or "formal," which describes the argument expression specified in the function call and the argument declaration specified in the function definition, respectively.  
  
 The term "variable" refers to a simple C-type data object. The term "object" refers to both C++ objects and variables; it is an inclusive term.  
  
## See Also  
 [C/C++ Preprocessor Reference](../vs140/C-C---Preprocessor-Reference.md)   
 [Phases of Translation](../vs140/Phases-of-Translation.md)