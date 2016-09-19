---
title: "internal (C# Reference)"
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
ms.assetid: 6ee0785c-d7c8-49b8-bb72-0a4dfbcb6461
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# internal (C# Reference)
The `internal` keyword is an [access modifier](../vs140/Access-Modifiers--C#-Reference-.md) for types and type members. Internal types or members are accessible only within files in the same assembly, as in this example:  
  
```  
public class BaseClass   
{  
    // Only accessible within the same assembly  
    internal static int x = 0;  
}  
```  
  
 Types or members that have access modifier `protected internal` can be accessed from the current assembly or from types that are derived from the containing class.  
  
 For a comparison of `internal` with the other access modifiers, see [Accessibility Levels](../vs140/Accessibility-Levels--C#-Reference-.md) and [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 For more information about assemblies, see [Assemblies and the Global Assembly Cache (C#)](../vs140/Assemblies-and-the-Global-Assembly-Cache--C#-and-Visual-Basic-.md).  
  
 A common use of internal access is in component-based development because it enables a group of components to cooperate in a private manner without being exposed to the rest of the application code. For example, a framework for building graphical user interfaces could provide `Control` and `Form` classes that cooperate by using members with internal access. Since these members are internal, they are not exposed to code that is using the framework.  
  
 It is an error to reference a type or a member with internal access outside the assembly within which it was defined.  
  
## Example  
 This example contains two files, `Assembly1.cs` and `Assembly1`_`a.cs`. The first file contains an internal base class, `BaseClass`. In the second file, an attempt to instantiate `BaseClass` will produce an error.  
  
```  
// Assembly1.cs  
// Compile with: /target:library  
internal class BaseClass   
{  
   public static int intM = 0;  
}  
```  
  
```  
// Assembly1_a.cs  
// Compile with: /reference:Assembly1.dll  
class TestAccess   
{  
   static void Main()   
   {  
      BaseClass myBase = new BaseClass();   // CS0122  
   }  
}  
```  
  
## Example  
 In this example, use the same files you used in example 1, and change the accessibility level of `BaseClass` to `public`. Also change the accessibility level of the member `IntM` to `internal`. In this case, you can instantiate the class, but you cannot access the internal member.  
  
```  
// Assembly2.cs  
// Compile with: /target:library  
public class BaseClass   
{  
   internal static int intM = 0;  
}  
```  
  
```  
// Assembly2_a.cs  
// Compile with: /reference:Assembly1.dll  
public class TestAccess   
{  
   static void Main()   
   {  
      BaseClass myBase = new BaseClass();   // Ok.  
      BaseClass.intM = 444;    // CS0117  
   }  
}  
```  
  
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
 [private (C# Programmer's Reference)](../vs140/private--C#-Reference-.md)   
 [protected (C# Programmer's Reference)](../vs140/protected--C#-Reference-.md)