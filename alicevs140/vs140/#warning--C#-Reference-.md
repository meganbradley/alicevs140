---
title: "#warning (C# Reference)"
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
ms.assetid: e6fb496d-bb8b-4018-baf6-5b60a0c8902b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #warning (C# Reference)
`#warning` lets you generate a level one warning from a specific location in your code. For example:  
  
```  
#warning Deprecated code in this method.  
```  
  
## Remarks  
 A common use of `#warning` is in a conditional directive. It is also possible to generate a user-defined error with [#error](../vs140/#error--C#-Reference-.md).  
  
## Example  
  
```  
// preprocessor_warning.cs  
// CS1030 expected  
#define DEBUG  
class MainClass   
{  
    static void Main()   
    {  
#if DEBUG  
#warning DEBUG is defined  
#endif  
    }  
}  
```  
  
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Preprocessor Directives](../vs140/C#-Preprocessor-Directives.md)