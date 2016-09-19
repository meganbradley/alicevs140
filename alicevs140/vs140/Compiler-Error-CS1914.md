---
title: "Compiler Error CS1914"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e61361b6-4660-41fd-a574-cc48e1b3873c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1914
Static field 'name' cannot be assigned in an object initializer  
  
 Object initializers by definition initialize objects, or instances, of classes. They cannot be used to initialize a `static` field of a type. No matter how many instances of a class are created, there is only one copy of a `static` field.  
  
### To correct this error  
  
1.  Either change the field to an instance field in the type, or remove the attempt to initialize it from the object initializer.  
  
## Example  
 The following code generates CS1914 because the initializer tries to initialize the `TestClass.Number` field, which is `static`:  
  
```  
// cs1914.cs  
using System.Linq;  
public class TestClass  
{  
    public string Message { get; set; }  
    public static int Number { get; set; }      
}  
class Test  
{  
    static void Main()  
    {  
        TestClass b = new TestClass() { Message = "Hello", Number = "555-1212" }; // CS1914  
  
    }  
}  
```