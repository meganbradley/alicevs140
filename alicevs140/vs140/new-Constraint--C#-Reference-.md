---
title: "new Constraint (C# Reference)"
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
ms.assetid: 58850b64-cb97-4136-be50-1f3bc7fc1da9
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# new Constraint (C# Reference)
The `new` constraint specifies that any type argument in a generic class declaration must have a public parameterless constructor. To use the new constraint, the type cannot be abstract.  
  
## Example  
 Apply the `new` constraint to a type parameter when your generic class creates new instances of the type, as shown in the following example:  
  
 [!CODE [csrefKeywordsOperator#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#5)]  
  
## Example  
 When you use the `new()` constraint with other constraints, it must be specified last:  
  
 [!CODE [csrefKeywordsOperator#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#6)]  
  
 For more information, see [Constraints on Type Parameters (C# Programming Guide)](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 <xref:System.Collections.Generic?qualifyHint=False>   
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Operator Keywords](../vs140/Operator-Keywords--C#-Reference-.md)   
 [Generics (C# Programming Guide)](../Topic/Generics%20\(C%23%20Programming%20Guide\).md)