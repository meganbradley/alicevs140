---
title: "Constructors (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 2cd0ed07-d214-4125-8317-4f288af99f05
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constructors (F#)
This topic describes how to define and use constructors to create and initialize class and structure objects.  
  
## Construction of Class Objects  
 Objects of class types have constructors. There are two kinds of constructors. One is the primary constructor, whose parameters appear in parentheses just after the type name. You specify other, optional additional constructors by using the `new` keyword. Any such additional constructors must call the primary constructor.  
  
 The primary constructor contains `let` and `do` bindings that appear at the start of the class definition. A `let` binding declares private fields and methods of the class; a `do` binding executes code. For more information about `let` bindings in class constructors, see [Let Bindings in Classes](../vs140/let-Bindings-in-Classes--F#-.md). For more information about `do` bindings in constructors, see [Do Bindings in Classes](../vs140/do-Bindings-in-Classes--F#-.md).  
  
 Regardless of whether the constructor you want to call is a primary constructor or an additional constructor, you can create objects by using a `new` expression, with or without the optional `new` keyword. You initialize your objects together with constructor arguments, either by listing the arguments in order and separated by commas and enclosed in parentheses, or by using named arguments and values in parentheses. You can also set properties on an object during the construction of the object by using the property names and assigning values just as you use named constructor arguments.  
  
 The following code illustrates a class that has a constructor and various ways of creating objects.  
  
 [!CODE [FsLangRef2#3501](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#3501)]  
  
 The output is as follows.  
  
```  
Initialized object that has coordinates (1, 2, 3)  
Initialized object that has coordinates (4, 5, 6)  
Initialized object that has coordinates (7, 8, 9)  
Initialized object that has coordinates (0, 0, 0)  
```  
  
## Construction of Structures  
 Structures follow all the rules of classes. Therefore, you can have a primary constructor, and you can provide additional constructors by using `new`. However, there is one important difference between structures and classes: structures can have a default constructor (that is, one with no arguments) even if no primary constructor is defined. The default constructor initializes all the fields to the default value for that type, usually zero or its equivalent. Any constructors that you define for structures must have at least one argument so that they do not conflict with the default constructor.  
  
 Also, structures often have fields that are created by using the `val` keyword; classes can also have these fields. Structures and classes that have fields defined by using the `val` keyword can also be initialized in additional constructors by using record expressions, as shown in the following code.  
  
 [!CODE [FsLangRef2#3502](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#3502)]  
  
 For more information, see [Fields: the val Keyword](../Topic/Explicit%20Fields:%20The%20val%20Keyword%20\(F%23\).md).  
  
## Executing Side Effects in Constructors  
 A primary constructor in a class can execute code in a `do` binding. However, what if you have to execute code in an additional constructor, without a `do` binding? To do this, you use the `then` keyword.  
  
 [!CODE [FsLangRef2#3503](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#3503)]  
  
 The side effects of the primary constructor still execute. Therefore, the output is as follows.  
  
```  
Created a person object.  
Created a person object.  
Created an invalid person object.  
```  
  
## Self Identifiers in Constructors  
 In other members, you provide a name for the current object in the definition of each member. You can also put the self identifier on the first line of the class definition by using the `as` keyword immediately following the constructor parameters. The following example illustrates this syntax.  
  
 [!CODE [FsLangRef2#3504](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#3504)]  
  
 In additional constructors, you can also define a self identifier by putting the `as` clause right after the constructor parameters. The following example illustrates this syntax.  
  
 [!CODE [FsLangRef2#3505](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#3505)]  
  
 Problems can occur when you try to use an object before it is fully defined. Therefore, uses of the self identifier can cause the compiler to emit a warning and insert additional checks to ensure the members of an object are not accessed before the object is initialized. You should only use the self identifier in the `do` bindings of the primary constructor, or after the `then` keyword in additional constructors.  
  
 The name of the self identifier does not have to be `this`. It can be any valid identifier.  
  
## Assigning Values to Properties at Initialization  
 You can assign values to the properties of a class object in the initialization code by appending a list of assignments of the form `property = value` to the argument list for a constructor. This is shown in the following code example.  
  
 [!CODE [FsLangRef2#3506](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#3506)]  
  
 The following version of the previous code illustrates the combination of ordinary arguments, optional arguments, and property settings in one constructor call.  
  
 [!CODE [FsLangRef2#3507](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#3507)]  
  
## Static Constructors or Type Constructors  
 In addition to specifying code for creating objects, static `let` and `do` bindings can be authored in class types that execute before the type is first used to perform initialization at the type level. For more information, see [Let Bindings in Classes](../vs140/let-Bindings-in-Classes--F#-.md) and [Do Bindings in Classes](../vs140/do-Bindings-in-Classes--F#-.md).  
  
## See Also  
 [Members](../vs140/Members--F#-.md)