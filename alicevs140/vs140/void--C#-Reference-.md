---
title: "void (C# Reference)"
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
ms.assetid: 0d2d8a95-fe20-4fbd-bf5d-c1e54bce71d4
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# void (C# Reference)
When used as the return type for a method, `void` specifies that the method doesn't return a value.  
  
 `void` isn't allowed in the parameter list of a method. A method that takes no parameters and returns no value is declared as follows:  
  
```  
public void SampleMethod()  
{  
    // Body of the method.  
}  
  
```  
  
 `void` is also used in an unsafe context to declare a pointer to an unknown type. For more information, see [Pointer types](../vs140/Pointer-types--C#-Programming-Guide-.md).  
  
 `void` is an alias for the .NET Framework <xref:System.Void?qualifyHint=True> type.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Reference Types](../vs140/Reference-Types--C#-Reference-.md)   
 [Value Types](../Topic/Value%20Types%20\(C%23%20Reference\).md)   
 [Methods (C# Programming Guide)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)   
 [Unsafe Code and Pointers (C# Programming Guide)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md)