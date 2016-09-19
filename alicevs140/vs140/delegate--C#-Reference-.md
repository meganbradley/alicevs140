---
title: "delegate (C# Reference)"
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
ms.assetid: 0bb8cb6d-2f87-47c7-9d1f-d65c1cd01e9f
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# delegate (C# Reference)
The declaration of a delegate type is similar to a method signature. It has a return value and any number of parameters of any type:  
  
```  
public delegate void TestDelegate(string message);  
public delegate int TestDelegate(MyType m, long num);  
```  
  
 A `delegate` is a reference type that can be used to encapsulate a named or an anonymous method. Delegates are similar to function pointers in C++; however, delegates are type-safe and secure. For applications of delegates, see [Delegates](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md) and [Generic Delegates](../vs140/Generic-Delegates--C#-Programming-Guide-.md).  
  
## Remarks  
 Delegates are the basis for [Events](../Topic/Events%20\(C%23%20Programming%20Guide\).md).  
  
 A delegate can be instantiated by associating it either with a named or anonymous method. For more information, see [Named Methods](../vs140/Delegates-with-Named-vs.-Anonymous-Methods--C#-Programming-Guide-.md) and [Anonymous Methods](../vs140/Anonymous-Methods--C#-Programming-Guide-.md).  
  
 The delegate must be instantiated with a method or lambda expression that has a compatible return type and input parameters. For more information on the degree of variance that is allowed in the method signature, see [Variance in Generic Delegates](../vs140/Variance-in-Delegates--C#-and-Visual-Basic-.md). For use with anonymous methods, the delegate and the code to be associated with it are declared together. Both ways of instantiating delegates are discussed in this section.  
  
## Example  
 [!CODE [csrefKeywordsTypes#8](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#8)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Reference Types](../vs140/Reference-Types--C#-Reference-.md)   
 [Delegates (Visual C#)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)   
 [Events (C#)](../Topic/Events%20\(C%23%20Programming%20Guide\).md)   
 [Named Methods](../vs140/Delegates-with-Named-vs.-Anonymous-Methods--C#-Programming-Guide-.md)   
 [Anonymous Methods](../vs140/Anonymous-Methods--C#-Programming-Guide-.md)