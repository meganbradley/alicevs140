---
title: "Passing Value-Type Parameters (C# Programming Guide)"
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
ms.assetid: 193ab86f-5f9b-4359-ac29-7cdf8afad3a6
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Passing Value-Type Parameters (C# Programming Guide)
A [value-type](../Topic/Value%20Types%20\(C%23%20Reference\).md) variable contains its data directly as opposed to a [reference-type](../vs140/Reference-Types--C#-Reference-.md) variable, which contains a reference to its data. Passing a value-type variable to a method by value means passing a copy of the variable to the method. Any changes to the parameter that take place inside the method have no affect on the original data stored in the argument variable. If you want the called method to change the value of the parameter, you must pass it by reference, using the [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md) keyword. For simplicity, the following examples use `ref`.  
  
## Passing Value Types by Value  
 The following example demonstrates passing value-type parameters by value. The variable `n` is passed by value to the method `SquareIt`. Any changes that take place inside the method have no affect on the original value of the variable.  
  
 [!CODE [csProgGuideParameters#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideParameters#3)]  
  
 The variable `n` is a value type. It contains its data, the value `5`. When `SquareIt` is invoked, the contents of `n` are copied into the parameter `x`, which is squared inside the method. In `Main`, however, the value of `n` is the same after calling the `SquareIt` method as it was before. The change that takes place inside the method only affects the local variable `x`.  
  
## Passing Value Types by Reference  
 The following example is the same as the previous example, except that the argument is passed as a `ref` parameter. The value of the underlying argument, `n`, is changed when `x` is changed in the method.  
  
 [!CODE [csProgGuideParameters#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideParameters#4)]  
  
 In this example, it is not the value of `n` that is passed; rather, a reference to `n` is passed. The parameter `x` is not an [int](../Topic/int%20\(C%23%20Reference\).md); it is a reference to an `int`, in this case, a reference to `n`. Therefore, when `x` is squared inside the method, what actually is squared is what `x` refers to, `n`.  
  
## Swapping Value Types  
 A common example of changing the values of arguments is a swap method, where you pass two variables to the method, and the method swaps their contents. You must pass the arguments to the swap method by reference. Otherwise, you swap local copies of the parameters inside the method, and no change occurs in the calling method. The following example swaps integer values.  
  
 [!CODE [csProgGuideParameters#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideParameters#5)]  
  
 When you call the `SwapByRef` method, use the `ref` keyword in the call, as shown in the following example.  
  
 [!CODE [csProgGuideParameters#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideParameters#6)]  
  
## See Also  
 [C# Programming](../vs140/C#-Programming-Guide.md)   
 [Passing Parameters (C#)](../vs140/Passing-Parameters--C#-Programming-Guide-.md)   
 [Passing Reference-Type Parameters](../vs140/Passing-Reference-Type-Parameters--C#-Programming-Guide-.md)