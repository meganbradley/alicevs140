---
title: "Tokens (C++)"
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
ms.assetid: aa812fd0-6d47-4f3f-aee0-db002ee4d8b9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Tokens (C++)
A token is the smallest element of a C++ program that is meaningful to the compiler. The C++ parser recognizes these kinds of tokens: identifiers, keywords, literals, operators, punctuators, and other separators. A stream of these tokens makes up a translation unit.  
  
 Tokens are usually separated by *white space*. White space can be one or more:  
  
-   Blanks  
  
-   Horizontal or vertical tabs  
  
-   New lines  
  
-   Formfeeds  
  
-   Comments  
  
 The parser recognizes keywords, identifiers, literals, operators, and punctuators. For information on specific token types, see [Keywords](../vs140/Keywords--C---.md), [Identifiers](../vs140/Identifiers--C---.md), [Numeric, Boolean and Pointer Literals](../vs140/Numeric--Boolean-and-Pointer-Literals---C---.md), [String and Character Literals](../vs140/String-and-Character-Literals---C---.md), [User-Defined Literals](../vs140/User-Defined-Literals---C---.md), [C++ Built-in Operators, Precedence and Associativity](../vs140/C---Built-in-Operators--Precedence-and-Associativity.md), and [Punctuators](../vs140/Punctuators--C---.md). White space is ignored, except as required to separate tokens.  
  
 Preprocessing tokens are used in the preprocessing phases to generate the token stream passed to the compiler. The preprocessing token categories are header names, identifiers, preprocessing numbers, character literals, string literals, preprocessing operators and punctuators, and single non-white-space characters that do not match one of the other categories. Character and string literals can be user-defined literals. Preprocessing tokens can be separated by white space or comments.  
  
 The parser separates tokens from the input stream by creating the longest token possible using the input characters in a left-to-right scan. Consider this code fragment:  
  
```  
a = i+++j;  
```  
  
 The programmer who wrote the code might have intended either of these two statements:  
  
```  
a = i + (++j)  
  
a = (i++) + j  
```  
  
 Because the parser creates the longest token possible from the input stream, it chooses the second interpretation, making the tokens `i++`, `+`, and `j`.  
  
## See Also  
 [Lexical Conventions](../vs140/Lexical-Conventions.md)