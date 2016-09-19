---
title: "Properties (C# Programming Guide)"
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
ms.assetid: e295a8a2-b357-4ee7-a12e-385a44146fa8
caps.latest.revision: 40
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Properties (C# Programming Guide)
A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field. Properties can be used as if they are public data members, but they are actually special methods called *accessors*. This enables data to be accessed easily and still helps promote the safety and flexibility of methods.  
  
 In this example, the `TimePeriod` class stores a time period. Internally the class stores the time in seconds, but a property named `Hours` enables a client to specify a time in hours. The accessors for the `Hours` property perform the conversion between hours and seconds.  
  
## Example  
 [!CODE [csProgGuideProperties#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#1)]  
  
## Expression Body Definitions  
 It is common to have properties that simply return immediately with the result of an expression.  There is a syntax shortcut for defining these properties using `=>`:  
  
```c#  
public string Name => First + " " + Last;   
```  
  
 The property must be read only, and you do not use the `get` accessor keyword.  
  
## Properties Overview  
  
-   Properties enable a class to expose a public way of getting and setting values, while hiding implementation or verification code.  
  
-   A [get](../vs140/get--C#-Reference-.md) property accessor is used to return the property value, and a [set](../vs140/set--C#-Reference-.md) accessor is used to assign a new value. These accessors can have different access levels. For more information, see [Accessor Accessibility](../vs140/Restricting-Accessor-Accessibility--C#-Programming-Guide-.md).  
  
-   The [value](../vs140/value--C#-Reference-.md) keyword is used to define the value being assigned by the `set` accessor.  
  
-   Properties that do not implement a `set` accessor are read only.  
  
-   For simple properties that require no custom accessor code, consider the option of using auto-implemented properties. For more information, see [Auto-Implemented Properties (C# Programming Guide)](../vs140/Auto-Implemented-Properties--C#-Programming-Guide-.md).  
  
## Related Sections  
  
-   [Using Properties (c#)](../vs140/Using-Properties--C#-Programming-Guide-.md)  
  
-   [Interface Properties](../vs140/Interface-Properties--C#-Programming-Guide-.md)  
  
-   [Comparison Between Properties and Indexers](../vs140/Comparison-Between-Properties-and-Indexers--C#-Programming-Guide-.md)  
  
-   [Asymmetric Accessor Accessibility (C# Programmer's Reference)](../vs140/Restricting-Accessor-Accessibility--C#-Programming-Guide-.md)  
  
-   [Auto-Implemented Properties (C# Programming Guide)](../vs140/Auto-Implemented-Properties--C#-Programming-Guide-.md)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming](../vs140/C#-Programming-Guide.md)   
 [Using Properties (C# Programming Guide)](../vs140/Using-Properties--C#-Programming-Guide-.md)   
 [Indexers](../vs140/Indexers--C#-Programming-Guide-.md)