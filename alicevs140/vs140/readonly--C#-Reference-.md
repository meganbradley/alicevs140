---
title: "readonly (C# Reference)"
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
ms.assetid: 2f8081f6-0de2-4903-898d-99696c48d2f4
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# readonly (C# Reference)
The `readonly` keyword is a modifier that you can use on fields. When a field declaration includes a `readonly` modifier, assignments to the fields introduced by the declaration can only occur as part of the declaration or in a constructor in the same class.  
  
## Example  
 In this example, the value of the field `year` cannot be changed in the method `ChangeYear`, even though it is assigned a value in the class constructor:  
  
 [!CODE [csrefKeywordsModifiers#14](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#14)]  
  
 You can assign a value to a `readonly` field only in the following contexts:  
  
-   When the variable is initialized in the declaration, for example:  
  
    ```  
    public readonly int y = 5;  
    ```  
  
-   For an instance field, in the instance constructors of the class that contains the field declaration, or for a static field, in the static constructor of the class that contains the field declaration. These are also the only contexts in which it is valid to pass a `readonly` field as an [out](../vs140/out--C#-Reference-.md) or [ref](../vs140/ref--C#-Reference-.md) parameter.  
  
> [!NOTE]
>  The `readonly` keyword is different from the [const](../vs140/const--C#-Reference-.md) keyword. A `const` field can only be initialized at the declaration of the field. A `readonly` field can be initialized either at the declaration or in a constructor. Therefore, `readonly` fields can have different values depending on the constructor used. Also, while a `const` field is a compile-time constant, the `readonly` field can be used for runtime constants as in the following example:  
  
```  
public static readonly uint timeStamp = (uint)DateTime.Now.Ticks;  
```  
  
## Example  
 [!CODE [csrefKeywordsModifiers#15](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#15)]  
  
 In the preceding example, if you use a statement like this:  
  
 `p2.y = 66;        // Error`  
  
 you will get the compiler error message:  
  
 `The left-hand side of an assignment must be an l-value`  
  
 which is the same error you get when you attempt to assign a value to a constant.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [const (C# Programmer's Reference)](../vs140/const--C#-Reference-.md)   
 [Properties and Fields (C#)](../vs140/Fields--C#-Programming-Guide-.md)