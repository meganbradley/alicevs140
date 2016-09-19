---
title: "Compiler Error CS0267"
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
ms.assetid: 11aaab96-5838-4e36-9551-5b032a1089e1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0267
The partial modifier can only appear immediately before 'class', 'struct', or 'interface'  
  
 The placement of the **partial** modifier was incorrect in the declaration of the class, struct or interface. To fix the error, reorder the modifiers. For more information, see [Partial Class Definitions (C# Programmer's Reference)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md).  
  
 The following sample generates CS0267:  
  
```  
// CS0267.cs  
public partial class MyClass  
{  
   public MyClass()  
   {  
   }  
}  
  
partial public class MyClass  // CS0267  
// Try this line instead:  
// public partial class MyClass  
{  
   public void Foo()  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
```