---
title: "How to: Define a Class That Can Provide Identical Functionality on Different Data Types (Visual Basic)"
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
ms.assetid: a914adf8-e68f-4819-a6b1-200d1cf1c21c
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Define a Class That Can Provide Identical Functionality on Different Data Types (Visual Basic)
You can define a class from which you can create objects that provide identical functionality on different data types. To do this, you specify one or more *type parameters* in the definition. The class can then serve as a template for objects that use various data types. A class defined in this way is called a *generic class*.  
  
 The advantage of defining a generic class is that you define it just once, and your code can use it to create many objects that use a wide variety of data types. This results in better performance than defining the class with the `Object` type.  
  
 In addition to classes, you can also define and use generic structures, interfaces, procedures, and delegates.  
  
### To define a class with a type parameter  
  
1.  Define the class in the normal way.  
  
2.  Add `(Of` *typeparameter*`)` immediately after the class name to specify a type parameter.  
  
3.  If you have more than one type parameter, make a comma-separated list inside the parentheses. Do not repeat the `Of` keyword.  
  
4.  If your code performs operations on a type parameter other than simple assignment, follow that type parameter with an `As` clause to add one or more *constraints*. A constraint guarantees that the type supplied for that type parameter satisfies a requirement such as the following:  
  
    -   Supports an operation, such as `>`, that your code performs  
  
    -   Supports a member, such as a method, that your code accesses  
  
    -   Exposes a parameterless constructor  
  
     If you do not specify any constraints, the only operations and members your code can use are those supported by the [Object Data Type](../Topic/Object%20Data%20Type.md). For more information, see [Type List](../vs140/Type-List--Visual-Basic-.md).  
  
5.  Identify every class member that is to be declared with a supplied type, and declare it `As` `typeparameter`. This applies to internal storage, procedure parameters, and return values.  
  
6.  Be sure your code uses only operations and methods that are supported by any data type it can supply to `itemType`.  
  
     The following example defines a class that manages a very simple list. It holds the list in the internal array `items`, and the using code can declare the data type of the list elements. A parameterized constructor allows the using code to set the upper bound of `items`, and the default constructor sets this to 9 (for a total of 10 items).  
  
     [!CODE [VbVbalrDataTypes#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDataTypes#7)]  
  
     You can declare a class from `simpleList` to hold a list of `Integer` values, another class to hold a list of `String` values, and another to hold `Date` values. Except for the data type of the list members, objects created from all these classes behave identically.  
  
     The type argument that the using code supplies to `itemType` can be an intrinsic type such as `Boolean` or `Double`, a structure, an enumeration, or any type of class, including one that your application defines.  
  
     You can test the class `simpleList` with the following code.  
  
     [!CODE [VbVbalrDataTypes#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDataTypes#8)]  
  
## See Also  
 [Data Types in Visual Basic](../vs140/Data-Types-in-Visual-Basic.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6)   
 [Of](../Topic/Of%20Clause%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)   
 [How to: Use a Generic Class](../Topic/How%20to:%20Use%20a%20Generic%20Class%20\(Visual%20Basic\).md)   
 [Object Data Type](../Topic/Object%20Data%20Type.md)