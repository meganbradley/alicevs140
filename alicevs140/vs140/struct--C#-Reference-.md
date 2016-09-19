---
title: "struct (C# Reference)"
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
ms.assetid: ff3dd9b7-dc93-4720-8855-ef5558f65c7c
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# struct (C# Reference)
A `struct` type is a value type that is typically used to encapsulate small groups of related variables, such as the coordinates of a rectangle or the characteristics of an item in an inventory. The following example shows a simple struct declaration:  
  
```  
public struct Book  
{  
    public decimal price;  
    public string title;  
    public string author;  
}  
```  
  
## Remarks  
 Structs can also contain [constructors](../vs140/Constructors--C#-Programming-Guide-.md), [constants](../Topic/Constants%20\(C%23%20Programming%20Guide\).md), [fields](../vs140/Fields--C#-Programming-Guide-.md), [methods](../Topic/Methods%20\(C%23%20Programming%20Guide\).md), [properties](../vs140/Properties--C#-Programming-Guide-.md), [indexers](../vs140/Indexers--C#-Programming-Guide-.md), [operators](../Topic/Operators%20\(C%23%20Programming%20Guide\).md), [events](../Topic/Events%20\(C%23%20Programming%20Guide\).md), and [nested types](../vs140/Nested-Types--C#-Programming-Guide-.md), although if several such members are required, you should consider making your type a class instead.  
  
 For examples, see [Using Structs (C# Programming Guide)](../vs140/Using-Structs--C#-Programming-Guide-.md).  
  
 Structs can implement an interface but they cannot inherit from another struct. For that reason, struct members cannot be declared as `protected`.  
  
 For more information, see [Structs (C#)](../vs140/Structs--C#-Programming-Guide-.md).  
  
## Examples  
 For examples and more information, see [Using Structs (C# Programming Guide)](../vs140/Using-Structs--C#-Programming-Guide-.md).  
  
## C# Language Specification  
 For examples, see [Using Structs (C# Programming Guide)](../vs140/Using-Structs--C#-Programming-Guide-.md).  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Default Values Table](../vs140/Default-Values-Table--C#-Reference-.md)   
 [Built-in Types Table (Visual C#)](../Topic/Built-In%20Types%20Table%20\(C%23%20Reference\).md)   
 [Types](../vs140/Types--C#-Reference-.md)   
 [Value Types](../Topic/Value%20Types%20\(C%23%20Reference\).md)   
 [class](../vs140/class--C#-Reference-.md)   
 [interface (C# Programmer's Reference)](../vs140/interface--C#-Reference-.md)   
 [Objects, Classes and Structs (C# Programmer's Reference)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)