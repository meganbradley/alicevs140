---
title: "Auto-Implemented Properties (C# Programming Guide)"
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
ms.assetid: aa55fa97-ccec-431f-b5e9-5ac789fd32b7
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Auto-Implemented Properties (C# Programming Guide)
In C# 3.0 and later, auto-implemented properties make property-declaration more concise when no additional logic is required in the property accessors. They also enable client code to create objects. When you declare a property as shown in the following example, the compiler creates a private, anonymous backing field that can only be accessed through the property's `get` and `set` accessors.  
  
## Example  
 The following example shows a simple class that has some auto-implemented properties:  
  
 [!CODE [csProgGuideLINQ#28](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#28)]  
  
 In C# 6 and later, you can initialize auto-implemented properties similarly to fields:  
  
```c#  
public string FirstName { get; set; } = "Jane";  
```  
  
 The class that is shown in the previous example is mutable. Client code can change the values in objects after they are created. In complex classes that contain significant behavior (methods) as well as data, it is often necessary to have public properties. However, for small classes or structs that just encapsulate a set of values (data) and have little or no behaviors, you should either make the objects immutable by declaring the set accessor as [private](../vs140/private--C#-Reference-.md) (immutable to consumers) or by declaring only a get accessor (immutable everywhere except the constructor).  For more information, see [How to: Implement an Immutable Class or Struct with Auto-Implemented Properties (C# Programming Guide)](../vs140/How-to--Implement-a-Lightweight-Class-with-Auto-Implemented-Properties--C#-Programming-Guide-.md).  
  
 Attributes are permitted on auto-implemented properties but obviously not on the backing fields since those are not accessible from your source code. If you must use an attribute on the backing field of a property, just create a regular property.  
  
## See Also  
 [Properties (C# Programming Guide)](../vs140/Properties--C#-Programming-Guide-.md)   
 [Modifiers (C# Reference)](../vs140/Modifiers--C#-Reference-.md)