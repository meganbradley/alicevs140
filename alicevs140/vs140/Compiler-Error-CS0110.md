---
title: "Compiler Error CS0110"
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
ms.assetid: 0bfe7071-1194-4142-a1a1-6190ee92b1d4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0110
The evaluation of the constant value for 'const declaration' involves a circular definition  
  
 The declaration of a [const](../vs140/const--C#-Reference-.md) variable (`a`) cannot reference another const variable (`b`) that also references (`a`).  
  
 The following sample generates CS0110:  
  
```  
// CS0110.cs  
namespace MyNamespace  
{  
   public class A  
   {  
      public static void Main()  
      {  
      }  
   }  
  
   public class B : A  
   {  
      public const int i = c + 1;   // CS0110, c already references i  
      public const int c = i + 1;  
      // the following line would be OK  
      // public const int c = 10;  
   }  
}  
```  
  
## See Also  
 [Constants (C# Programmer's Reference)](../Topic/Constants%20\(C%23%20Programming%20Guide\).md)