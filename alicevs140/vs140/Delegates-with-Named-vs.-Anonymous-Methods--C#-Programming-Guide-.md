---
title: "Delegates with Named vs. Anonymous Methods (C# Programming Guide)"
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
ms.assetid: 98fa8c61-66b6-4146-986c-3236c4045733
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Delegates with Named vs. Anonymous Methods (C# Programming Guide)
A [delegate](../vs140/delegate--C#-Reference-.md) can be associated with a named method. When you instantiate a delegate by using a named method, the method is passed as a parameter, for example:  
  
 [!CODE [csProgGuideDelegates#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#1)]  
  
 This is called using a named method. Delegates constructed with a named method can encapsulate either a [static](../vs140/static--C#-Reference-.md) method or an instance method. Named methods are the only way to instantiate a delegate in earlier versions of C#. However, in a situation where creating a new method is unwanted overhead, C# enables you to instantiate a delegate and immediately specify a code block that the delegate will process when it is called. The block can contain either a lambda expression or an anonymous method. For more information, see [Anonymous Functions (C# Programming Guide)](../vs140/Anonymous-Functions--C#-Programming-Guide-.md).  
  
## Remarks  
 The method that you pass as a delegate parameter must have the same signature as the delegate declaration.  
  
 A delegate instance may encapsulate either static or instance method.  
  
 Although the delegate can use an [out](../vs140/out--C#-Reference-.md) parameter, we do not recommend its use with multicast event delegates because you cannot know which delegate will be called.  
  
## Example 1  
 The following is a simple example of declaring and using a delegate. Notice that both the delegate, `Del`, and the associated method, `MultiplyNumbers`, have the same signature  
  
 [!CODE [csProgGuideDelegates#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#2)]  
  
## Example 2  
 In the following example, one delegate is mapped to both static and instance methods and returns specific information from each.  
  
 [!CODE [csProgGuideDelegates#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#3)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Delegates (Visual C#)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)   
 [Anonymous Methods (C# Programming Guide)](../vs140/Anonymous-Methods--C#-Programming-Guide-.md)   
 [How to: Combine Delegates (Multicast Delegates)(C# Programming Guide)](../Topic/How%20to:%20Combine%20Delegates%20\(Multicast%20Delegates\)\(C%23%20Programming%20Guide\).md)   
 [Events (C# Programming Guide)](../Topic/Events%20\(C%23%20Programming%20Guide\).md)