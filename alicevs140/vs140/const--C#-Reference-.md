---
title: "const (C# Reference)"
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
ms.assetid: 79eb447c-117b-4418-933f-97c50aa472db
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# const (C# Reference)
You use the `const` keyword to declare a constant field or a constant local. Constant fields and locals aren't variables and may not be modified. Constants can be numbers, Boolean values, strings, or a null reference. Don’t create a constant to represent information that you expect to change at any time. For example, don’t use a constant field to store the price of a service, a product version number, or the brand name of a company. These values can change over time, and because compilers propagate constants, other code compiled with your libraries will have to be recompiled to see the changes. See also the [readonly](../vs140/readonly--C#-Reference-.md) keyword. For example:  
  
```  
  
      const int x = 0;  
public const double gravitationalConstant = 6.673e-11;  
private const string productName = "Visual C#";  
```  
  
## Remarks  
 The type of a constant declaration specifies the type of the members that the declaration introduces. The initializer of a constant local or a constant field must be a constant expression that can be implicitly converted to the target type.  
  
 A constant expression is an expression that can be fully evaluated at compile time. Therefore, the only possible values for constants of reference types are `string` and a null reference.  
  
 The constant declaration can declare multiple constants, such as:  
  
```  
public const double x = 1.0, y = 2.0, z = 3.0;  
```  
  
 The `static` modifier is not allowed in a constant declaration.  
  
 A constant can participate in a constant expression, as follows:  
  
```  
public const int c1 = 5;  
public const int c2 = c1 + 100;  
```  
  
> [!NOTE]
>  The [readonly](../vs140/readonly--C#-Reference-.md) keyword differs from the `const` keyword. A `const` field can only be initialized at the declaration of the field. A `readonly` field can be initialized either at the declaration or in a constructor. Therefore, `readonly` fields can have different values depending on the constructor used. Also, although a `const` field is a compile-time constant, the `readonly` field can be used for run-time constants, as in this line: `public static readonly uint l1 = (uint)DateTime.Now.Ticks;`  
  
## Example  
 [!CODE [csrefKeywordsModifiers#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#5)]  
  
## Example  
 This example demonstrates how to use constants as local variables.  
  
 [!CODE [csrefKeywordsModifiers#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#6)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [readonly](../vs140/readonly--C#-Reference-.md)