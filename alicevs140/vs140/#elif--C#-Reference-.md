---
title: "#elif (C# Reference)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 731d78df-08e0-4d51-b8c8-f193c27de13f
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #elif (C# Reference)
`#elif` lets you create a compound conditional directive. The `#elif` expression will be evaluated if neither the preceding [#if](../vs140/#if--C#-Reference-.md) nor any preceding, optional, `#elif` directive expressions evaluate to `true`. If a `#elif` expression evaluates to `true`, the compiler evaluates all the code between the `#elif` and the next conditional directive. For example:  
  
```  
#define VC7  
//...  
#if debug  
    Console.Writeline("Debug build");  
#elif VC7  
    Console.Writeline("Visual Studio 7");  
#endif  
```  
  
 You can use the operators `==` (equality), `!=` (inequality), `&&` (and), and `||` (or), to evaluate multiple symbols. You can also group symbols and operators with parentheses.  
  
## Remarks  
 `#elif` is equivalent to using:  
  
```  
#else  
#if  
```  
  
 Using `#elif` is simpler, because each `#if` requires a [#endif](../vs140/#endif--C#-Reference-.md), whereas a `#elif` can be used without a matching `#endif`.  
  
 See [#if](../vs140/#if--C#-Reference-.md) for an example of how to use `#elif`.  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Preprocessor Directives](../vs140/C#-Preprocessor-Directives.md)