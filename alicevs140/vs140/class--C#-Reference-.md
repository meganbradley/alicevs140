---
title: "class (C# Reference)"
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
ms.assetid: b95d8815-de18-4c3f-a8cc-a0a53bdf8690
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# class (C# Reference)
Classes are declared using the keyword `class`, as shown in the following example:  
  
```  
  
      class TestClass  
{  
    // Methods, properties, fields, events, delegates   
    // and nested classes go here.  
}  
```  
  
## Remarks  
 Only single inheritance is allowed in C#. In other words, a class can inherit implementation from one base class only. However, a class can implement more than one interface. The following table shows examples of class inheritance and interface implementation:  
  
|Inheritance|Example|  
|-----------------|-------------|  
|None|`class ClassA { }`|  
|Single|`class DerivedClass: BaseClass { }`|  
|None, implements two interfaces|`class ImplClass: IFace1, IFace2 { }`|  
|Single, implements one interface|`class ImplDerivedClass: BaseClass, IFace1 { }`|  
  
 Classes that you declare directly within a namespace, not nested within other classes, can be either [public](../vs140/public--C#-Reference-.md) or [internal](../vs140/internal--C#-Reference-.md). Classes are `internal` by default.  
  
 Class members, including nested classes, can be [public](../vs140/public--C#-Reference-.md), `protected internal`, [protected](../vs140/protected--C#-Reference-.md), [internal](../vs140/internal--C#-Reference-.md), or [private](../vs140/private--C#-Reference-.md). Members are [private](../vs140/private--C#-Reference-.md) by default.  
  
 For more information, see [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 You can declare generic classes that have type parameters. For more information, see [Generic Classes](../Topic/Generic%20Classes%20\(C%23%20Programming%20Guide\).md).  
  
 A class can contain declarations of the following members:  
  
-   [Constructors](../vs140/Constructors--C#-Programming-Guide-.md)  
  
-   [Destructors](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md)  
  
-   [Constants](../Topic/Constants%20\(C%23%20Programming%20Guide\).md)  
  
-   [Fields](../vs140/Fields--C#-Programming-Guide-.md)  
  
-   [Methods](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)  
  
-   [Properties](../vs140/Properties--C#-Programming-Guide-.md)  
  
-   [Indexers](../vs140/Indexers--C#-Programming-Guide-.md)  
  
-   [Operators](../Topic/Operators%20\(C%23%20Programming%20Guide\).md)  
  
-   [Events](../Topic/Events%20\(C%23%20Programming%20Guide\).md)  
  
-   [Delegates](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)  
  
-   [Classes](../vs140/Classes--C#-Programming-Guide-.md)  
  
-   [Interfaces](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)  
  
-   [Structs](../vs140/Structs--C#-Programming-Guide-.md)  
  
## Example  
 The following example demonstrates declaring class fields, constructors, and methods. It also demonstrates object instantiation and printing instance data. In this example, two classes are declared, the `Child` class, which contains two private fields (`name` and `age`) and two public methods. The second class, `StringTest`, is used to contain `Main`.  
  
 [!CODE [csrefKeywordsTypes#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#5)]  
  
## Comments  
 Notice, in the preceding example, that the private fields (`name` and `age`) can only be accessed through the public methods of the `Child` class. For example, you cannot print the child's name, from the `Main` method, using a statement like this:  
  
```  
Console.Write(child1.name);   // Error  
```  
  
 Accessing private members of `Child` from `Main` would only be possible if `Main` were a member of the class.  
  
 Types declared inside a class without an access modifier default to `private`, so the data members in this example would still be `private` if the keyword were removed.  
  
 Finally, notice that for the object created using the default constructor (`child3`), the age field was initialized to zero by default.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Reference Types](../vs140/Reference-Types--C#-Reference-.md)