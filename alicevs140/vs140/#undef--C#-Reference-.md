---
title: "#undef (C# Reference)"
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
ms.assetid: 686c92d2-7194-4be4-b2f4-80091712d513
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #undef (C# Reference)
`#undef` lets you undefine a symbol, such that, by using the symbol as the expression in a [#if](../vs140/#if--C#-Reference-.md) directive, the expression will evaluate to `false`.  
  
 A symbol can be defined either with the [#define](../vs140/#define--C#-Reference-.md) directive or the [/define](../Topic/-define%20\(C%23%20Compiler%20Options\).md) compiler option. The `#undef` directive must appear in the file before you use any statements that are not also directives.  
  
## Example  
  
```  
// preprocessor_undef.cs  
// compile with: /d:DEBUG  
#undef DEBUG  
using System;  
class MyClass   
{  
    static void Main()   
    {  
#if DEBUG  
        Console.WriteLine("DEBUG is defined");  
#else  
        Console.WriteLine("DEBUG is not defined");  
#endif  
    }  
}  
```  
  
 **DEBUG is not defined**   
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Preprocessor Directives](../vs140/C#-Preprocessor-Directives.md)