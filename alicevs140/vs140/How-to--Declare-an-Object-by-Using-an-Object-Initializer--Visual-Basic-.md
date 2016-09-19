---
title: "How to: Declare an Object by Using an Object Initializer (Visual Basic)"
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
ms.assetid: 0f53a553-efd6-466d-80bf-6b679e5cd174
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Declare an Object by Using an Object Initializer (Visual Basic)
Object initializers enable you to declare and instantiate an instance of a class in a single statement. In addition, you can initialize one or more members of the instance at the same time, without invoking a parameterized constructor.  
  
 When you use an object initializer to create an instance of a named type, the default constructor for the class is called, followed by initialization of designated members in the order you specify.  
  
 The following procedure shows how to create an instance of a `Student` class in three different ways. The class has first name, last name, and class year properties, among others. Each of the three declarations creates a new instance of `Student`, with property `First` set to "Michael", property `Last` set to "Tucker", and all other members set to their default values. The result of each declaration in the procedure is equivalent to the following example, which does not use an object initializer.  
  
 [!CODE [VbVbalrObjectInit#20](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#20)]  
  
 For an implementation of the `Student` class, see [How to: Create a List of Items](../vs140/How-to--Create-a-List-of-Items.md). You can copy the code from that topic to set up the class and create a list of `Student` objects to work with.  
  
### To create an object of a named class by using an object initializer  
  
1.  Begin the declaration as if you planned to use a constructor.  
  
     `Dim student1 As New Student`  
  
2.  Type the keyword `With`, followed by an initialization list in braces.  
  
     `Dim student1 As New Student With { <initialization list> }`  
  
3.  In the initialization list, include each property that you want to initialize and assign an initial value to it. The name of the property is preceded by a period.  
  
     [!CODE [VbVbalrObjectInit#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#21)]  
  
     You can initialize one or more members of the class.  
  
4.  Alternatively, you can declare a new instance of the class and then assign a value to it. First, declare an instance of `Student`:  
  
     `Dim student2 As Student`  
  
5.  Begin the creation of an instance of `Student` in the normal way.  
  
     `Dim student2 As Student = New Student`  
  
6.  Type `With` and then an object initializer to initialize one or more members of the new instance.  
  
     [!CODE [VbVbalrObjectInit#22](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#22)]  
  
7.  You can simplify the definition in the previous step by omitting `As Student`. If you do this, the compiler determines that `student3` is an instance of `Student` by using local type inference.  
  
     [!CODE [VbVbalrObjectInit#23](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrObjectInit#23)]  
  
     For more information, see [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md).  
  
## See Also  
 [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md)   
 [How to: Create a List of Items](../vs140/How-to--Create-a-List-of-Items.md)   
 [Object Initializers](../vs140/Object-Initializers--Named-and-Anonymous-Types--Visual-Basic-.md)   
 [Anonymous Types (Visual Basic)](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)