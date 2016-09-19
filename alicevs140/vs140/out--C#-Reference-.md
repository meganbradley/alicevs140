---
title: "out (C# Reference)"
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
ms.assetid: 7e911a0c-3f98-4536-87be-d539b7536ca8
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# out (C# Reference)
You can use the `out` contextual keyword in two contexts (each is a link to detailed information), as a [parameter modifier](../vs140/out-parameter-modifier--C#-Reference-.md) or in [generic type parameter declarations](../Topic/out%20\(Generic%20Modifier\)%20\(C%23%20Reference\).md) in interfaces and delegates.  This topic discusses the parameter modifier, but you can see [this other topic](../Topic/out%20\(Generic%20Modifier\)%20\(C%23%20Reference\).md) for information on the generic type parameter declarations.  
  
 The `out` keyword causes arguments to be passed by reference. This is like the [ref](../vs140/ref--C#-Reference-.md) keyword, except that `ref` requires that the variable be initialized before it is passed. To use an `out` parameter, both the method definition and the calling method must explicitly use the `out` keyword. For example:  
  
 [!CODE [csrefKeywordsMethodParams#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#1)]  
  
 Although variables passed as `out` arguments do not have to be initialized before being passed, the called method is required to assign a value before the method returns.  
  
 Although the `ref` and `out` keywords cause different run-time behavior, they are not considered part of the method signature at compile time. Therefore, methods cannot be overloaded if the only difference is that one method takes a `ref` argument and the other takes an `out` argument. The following code, for example, will not compile:  
  
 [!CODE [csrefKeywordsMethodParams#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#2)]  
  
 Overloading can be done, however, if one method takes a `ref` or `out` argument and the other uses neither, like this:  
  
 [!CODE [csrefKeywordsMethodParams#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#3)]  
  
 Properties are not variables and therefore cannot be passed as `out` parameters.  
  
 For information about passing arrays, see [Passing Arrays Using ref and out](../vs140/Passing-Arrays-Using-ref-and-out--C#-Programming-Guide-.md).  
  
 You can't use the `ref` and `out` keywords for the following kinds of methods:  
  
-   Async methods, which you define by using the [async](../Topic/async%20\(C%23%20Reference\).md) modifier.  
  
-   Iterator methods, which include a [yield return](../Topic/yield%20\(C%23%20Reference\).md) or `yield break` statement.  
  
## Example  
 Declaring an `out` method is useful when you want a method to return multiple values. The following example uses `out` to return three variables with a single method call. Note that the third argument is assigned to null. This enables methods to return values optionally.  
  
 [!CODE [csrefKeywordsMethodParams#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#4)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)