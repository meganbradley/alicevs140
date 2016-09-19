---
title: "Anonymous Methods (C# Programming Guide)"
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
ms.assetid: a62441fa-f0a3-4acb-9aa6-93762a635275
caps.latest.revision: 33
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Anonymous Methods (C# Programming Guide)
In versions of C# before 2.0, the only way to declare a [delegate](../vs140/delegate--C#-Reference-.md) was to use [named methods](../vs140/Delegates-with-Named-vs.-Anonymous-Methods--C#-Programming-Guide-.md). C# 2.0 introduced anonymous methods and in C# 3.0 and later, lambda expressions supersede anonymous methods as the preferred way to write inline code. However, the information about anonymous methods in this topic also applies to lambda expressions. There is one case in which an anonymous method provides functionality not found in lambda expressions. Anonymous methods enable you to omit the parameter list. This means that an anonymous method can be converted to delegates with a variety of signatures. This is not possible with lambda expressions. For more information specifically about lambda expressions, see [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md).  
  
 Creating anonymous methods is essentially a way to pass a code block as a delegate parameter. Here are two examples:  
  
 [!CODE [csProgGuideDelegates#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#6)]  
  
 [!CODE [csProgGuideDelegates#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#5)]  
  
 By using anonymous methods, you reduce the coding overhead in instantiating delegates because you do not have to create a separate method.  
  
 For example, specifying a code block instead of a delegate can be useful in a situation when having to create a method might seem an unnecessary overhead. A good example would be when you start a new thread. This class creates a thread and also contains the code that the thread executes without creating an additional method for the delegate.  
  
 [!CODE [csProgGuideDelegates#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#7)]  
  
## Remarks  
 The scope of the parameters of an anonymous method is the *anonymous-method-block*.  
  
 It is an error to have a jump statement, such as [goto](../vs140/goto--C#-Reference-.md), [break](../vs140/break--C#-Reference-.md), or [continue](../vs140/continue--C#-Reference-.md), inside the anonymous method block if the target is outside the block. It is also an error to have a jump statement, such as `goto`, `break`, or `continue`, outside the anonymous method block if the target is inside the block.  
  
 The local variables and parameters whose scope contains an anonymous method declaration are called *outer* variables of the anonymous method. For example, in the following code segment, `n` is an outer variable:  
  
 [!CODE [csProgGuideDelegates#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#8)]  
  
 A reference to the outer variable `n` is said to be *captured* when the delegate is created. Unlike local variables, the lifetime of a captured variable extends until the delegates that reference the anonymous methods are eligible for garbage collection.  
  
 An anonymous method cannot access the [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md) parameters of an outer scope.  
  
 No unsafe code can be accessed within the *anonymous-method-block*.  
  
 Anonymous methods are not allowed on the left side of the [is](../vs140/is--C#-Reference-.md) operator.  
  
## Example  
 The following example demonstrates two ways of instantiating a delegate:  
  
-   Associating the delegate with an anonymous method.  
  
-   Associating the delegate with a named method (`DoWork`).  
  
 In each case, a message is displayed when the delegate is invoked.  
  
 [!CODE [csProgGuideDelegates#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#4)]  
  
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming](../vs140/C#-Programming-Guide.md)   
 [Delegates (Visual C#)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)   
 [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [Unsafe Code and Pointers (C# Programming Guide)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md)   
 [Methods (C# Programming Guide)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)   
 [Named Methods (C# Programming Guide)](../vs140/Delegates-with-Named-vs.-Anonymous-Methods--C#-Programming-Guide-.md)