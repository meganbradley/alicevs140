---
title: "New Operator (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d7d566d7-fe0e-4336-91f7-641a542de4d0
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# New Operator (Visual Basic)
Introduces a `New` clause to create a new object instance, specifies a constructor constraint on a type parameter, or identifies a `Sub` procedure as a class constructor.  
  
## Remarks  
 In a declaration or assignment statement, a `New` clause must specify a defined class from which the instance can be created. This means that the class must expose one or more constructors that the calling code can access.  
  
 You can use a `New` clause in a declaration statement or an assignment statement. When the statement runs, it calls the appropriate constructor of the specified class, passing any arguments you have supplied. The following example demonstrates this by creating instances of a `Customer` class that has two constructors, one that takes no parameters and one that takes a string parameter.  
  
 [!CODE [VbVbalrKeywords#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#11)]  
  
 Since arrays are classes, `New` can create a new array instance, as shown in the following examples.  
  
 [!CODE [VbVbalrKeywords#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#12)]  
  
 The common language runtime (CLR) throws an <xref:System.OutOfMemoryException?qualifyHint=False> error if there is insufficient memory to create the new instance.  
  
> [!NOTE]
>  The `New` keyword is also used in type parameter lists to specify that the supplied type must expose an accessible parameterless constructor. For more information about type parameters and constraints, see [Type List](../vs140/Type-List--Visual-Basic-.md).  
  
 To create a constructor procedure for a class, set the name of a `Sub` procedure to the `New` keyword. For more information, see [Object Lifetime: How Objects Are Created and Destroyed](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md).  
  
 The `New` keyword can be used in these contexts:  
  
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)  
  
 [Of](../Topic/Of%20Clause%20\(Visual%20Basic\).md)  
  
 [Sub Statement (Visual Basic)](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 <xref:System.OutOfMemoryException?qualifyHint=False>   
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Object Lifetime: How Objects Are Created and Destroyed](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md)