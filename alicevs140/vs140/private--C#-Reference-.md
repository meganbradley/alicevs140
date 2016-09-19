---
title: "private (C# Reference)"
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
ms.assetid: 654c0bb8-e6ac-4086-bf96-7474fa6aa1c8
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# private (C# Reference)
The `private` keyword is a member access modifier. Private access is the least permissive access level. Private members are accessible only within the body of the class or the struct in which they are declared, as in this example:  
  
```  
class Employee  
{  
    private int i;  
    double d;   // private access by default  
}  
```  
  
 Nested types in the same body can also access those private members.  
  
 It is a compile-time error to reference a private member outside the class or the struct in which it is declared.  
  
 For a comparison of `private` with the other access modifiers, see [Accessibility Levels](../vs140/Accessibility-Levels--C#-Reference-.md) and [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 In this example, the `Employee` class contains two private data members, `name` and `salary`. As private members, they cannot be accessed except by member methods. Public methods named `GetName` and `Salary` are added to allow controlled access to the private members. The `name` member is accessed by way of a public method, and the `salary` member is accessed by way of a public read-only property. (See [Properties (C# Programming Guide)](../vs140/Properties--C#-Programming-Guide-.md) for more information.)  
  
 [!CODE [csrefKeywordsModifiers#10](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#10)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Access Modifiers](../vs140/Access-Modifiers--C#-Reference-.md)   
 [Accessibility Levels](../vs140/Accessibility-Levels--C#-Reference-.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [public (C# Programmer's Reference)](../vs140/public--C#-Reference-.md)   
 [protected (C# Programmer's Reference)](../vs140/protected--C#-Reference-.md)   
 [internal (C# Programmer's Reference)](../vs140/internal--C#-Reference-.md)