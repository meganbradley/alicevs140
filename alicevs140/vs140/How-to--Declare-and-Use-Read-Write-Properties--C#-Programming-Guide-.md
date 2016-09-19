---
title: "How to: Declare and Use Read Write Properties (C# Programming Guide)"
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
ms.assetid: a4962fef-af7e-4c4b-a929-4ae4d646ab8a
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Declare and Use Read Write Properties (C# Programming Guide)
Properties provide the convenience of public data members without the risks that come with unprotected, uncontrolled, and unverified access to an object's data. This is accomplished through *accessors*: special methods that assign and retrieve values from the underlying data member. The [set](../vs140/set--C#-Reference-.md) accessor enables data members to be assigned, and the [get](../vs140/get--C#-Reference-.md) accessor retrieves data member values.  
  
 This sample shows a `Person` class that has two properties: `Name` (string) and `Age` (int). Both properties provide `get` and `set` accessors, so they are considered read/write properties.  
  
## Example  
 [!CODE [csProgGuideObjects#33](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#33)]  
  
## Robust Programming  
 In the previous example, the `Name` and `Age` properties are [public](../vs140/public--C#-Reference-.md) and include both a `get` and a `set` accessor. This allows any object to read and write these properties. It is sometimes desirable, however, to exclude one of the accessors. Omitting the `set` accessor, for example, makes the property read-only:  
  
 [!CODE [csProgGuideObjects#87](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#87)]  
  
 Alternatively, you can expose one accessor publicly but make the other private or protected. For more information, see [Asymmetric Accessor Accessibility](../vs140/Restricting-Accessor-Accessibility--C#-Programming-Guide-.md).  
  
 Once the properties are declared, they can be used as if they were fields of the class. This allows for a very natural syntax when both getting and setting the value of a property, as in the following statements:  
  
 [!CODE [csProgGuideObjects#35](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#35)]  
  
 Note that in a property `set` method a special `value` variable is available. This variable contains the value that the user specified, for example:  
  
 [!CODE [csProgGuideObjects#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#36)]  
  
 Notice the clean syntax for incrementing the `Age` property on a `Person` object:  
  
 [!CODE [csProgGuideObjects#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#37)]  
  
 If separate `set` and `get` methods were used to model properties, the equivalent code might look like this:  
  
```  
person.SetAge(person.GetAge() + 1);   
```  
  
 The `ToString` method is overridden in this example:  
  
 [!CODE [csProgGuideObjects#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#38)]  
  
 Notice that `ToString` is not explicitly used in the program. It is invoked by default by the `WriteLine` calls.  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Properties (C# Programming Guide)](../vs140/Properties--C#-Programming-Guide-.md)   
 [Objects, Classes, and Structs (Visual C#)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)