---
title: "#error Directive (C-C++)"
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
H1: #error Directive (C/C++)
ms.assetid: d550a802-ff19-4347-9597-688935d23b2b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #error Directive (C-C++)
The `#error` directive emits a user-specified error message at compile time and then terminates the compilation.  
  
## Syntax  
  
```  
#errortoken-string  
```  
  
## Remarks  
 The error message that this directive emits includes the *token-string* parameter. The `token-string` parameter is not subject to macro expansion. This directive is most useful during preprocessing for notifying the developer of a program inconsistency or the violation of a constraint. The following example demonstrates error processing during preprocessing:  
  
```  
#if !defined(__cplusplus)  
#error C++ compiler required.  
#endif  
```  
  
## See Also  
 [Preprocessor Directives](../vs140/Preprocessor-Directives.md)