---
title: "Fields (C# Programming Guide)"
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
ms.assetid: 3cbb2f61-75f8-4cce-b4ef-f5d1b3de0db7
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fields (C# Programming Guide)
A *field* is a variable of any type that is declared directly in a [class](../vs140/class--C#-Reference-.md) or [struct](../vs140/struct--C#-Reference-.md). Fields are *members* of their containing type.  
  
 A class or struct may have instance fields or static fields or both. Instance fields are specific to an instance of a type. If you have a class T, with an instance field F, you can create two objects of type T, and modify the value of F in each object without affecting the value in the other object. By contrast, a static field belongs to the class itself, and is shared among all instances of that class. Changes made from instance A will be visibly immediately to instances B and C if they access the field.  
  
 Generally, you should use fields only for variables that have private or protected accessibility. Data that your class exposes to client code should be provided through [methods](../Topic/Methods%20\(C%23%20Programming%20Guide\).md), [properties](../vs140/Properties--C#-Programming-Guide-.md) and [indexers](../vs140/Indexers--C#-Programming-Guide-.md). By using these constructs for indirect access to internal fields, you can guard against invalid input values. A private field that stores the data exposed by a public property is called a *backing store* or *backing field*.  
  
 Fields typically store the data that must be accessible to more than one class method and must be stored for longer than the lifetime of any single method. For example, a class that represents a calendar date might have three integer fields: one for the month, one for the day, and one for the year. Variables that are not used outside the scope of a single method should be declared as *local variables* within the method body itself.  
  
 Fields are declared in the class block by specifying the access level of the field, followed by the type of the field, followed by the name of the field. For example:  
  
 [!CODE [csProgGuideObjects#61](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#61)]  
  
 To access a field in an object, add a period after the object name, followed by the name of the field, as in `objectname.fieldname`. For example:  
  
 [!CODE [csProgGuideObjects#62](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#62)]  
  
 A field can be given an initial value by using the assignment operator when the field is declared. To automatically assign the `day` field to `"Monday"`, for example, you would declare `day` as in the following example:  
  
 [!CODE [csProgGuideObjects#63](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#63)]  
  
 Fields are initialized immediately before the constructor for the object instance is called. If the constructor assigns the value of a field, it will overwrite any value given during field declaration. For more information, see [Using Constructors](../Topic/Using%20Constructors%20\(C%23%20Programming%20Guide\).md).  
  
> [!NOTE]
>  A field initializer cannot refer to other instance fields.  
  
 Fields can be marked as [public](../vs140/public--C#-Reference-.md), [private](../vs140/private--C#-Reference-.md), [protected](../vs140/protected--C#-Reference-.md), [internal](../vs140/internal--C#-Reference-.md), or `protected internal`. These access modifiers define how users of the class can access the fields. For more information, see [Access Modifiers](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 A field can optionally be declared [static](../vs140/static--C#-Reference-.md). This makes the field available to callers at any time, even if no instance of the class exists. For more information, see [Static Classes and Static Class Members](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md).  
  
 A field can be declared [readonly](../vs140/readonly--C#-Reference-.md). A read-only field can only be assigned a value during initialization or in a constructor. A `static``readonly` field is very similar to a constant, except that the C# compiler does not have access to the value of a static read-only field at compile time, only at run time. For more information, see [Constants](../Topic/Constants%20\(C%23%20Programming%20Guide\).md).  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Classes and Structs (Visual C#)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Constructors and Destructors (Visual C#)](../Topic/Using%20Constructors%20\(C%23%20Programming%20Guide\).md)   
 [Inheritance (Visual C#)](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md)   
 [Access Modifiers (Visual C#)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [Abstract and Sealed Classes and Class Members (Visual C#)](../vs140/Abstract-and-Sealed-Classes-and-Class-Members--C#-Programming-Guide-.md)