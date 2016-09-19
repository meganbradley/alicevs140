---
title: "Compiler Error CS1730"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 20900ca0-702f-4f35-9a60-2dee9cb11902
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1730
Assembly and module attributes must precede all other elements defined in a file except using clauses and extern alias declarations.  
  
 An attribute applied at the assembly level cannot appear after any type definitions.  
  
### To correct this error  
  
1.  Move the attribute to the top of the file, but below the `using` directives and `extern` alias declarations.  
  
## Example  
 The following code generates CS1730:  
  
```  
// cs1730.cs  
class Test  
{  
}  
[assembly: System.Attribute] // CS1730  
```  
  
## See Also  
 [Attributes (C# Programming Guide)](../vs140/Attributes--C#-and-Visual-Basic-.md)