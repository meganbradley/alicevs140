---
title: "Compiler Error CS0214"
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
ms.assetid: be1ef909-a53e-485f-a79b-b1cc56cead15
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0214
Pointers and fixed size buffers may only be used in an unsafe context  
  
 Pointers can only be used with the [unsafe](../vs140/unsafe--C#-Reference-.md) keyword. For more information, see [Unsafe Code and Pointers (C# Programmer's Reference)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md).  
  
 The following sample generates CS0214:  
  
```  
// CS0214.cs  
// compile with: /target:library /unsafe  
public struct S  
{  
   public int a;  
}  
  
public class MyClass  
{  
   public static void Test()  
   {  
      S s = new S();  
      S * s2 = &s;    // CS0214  
      s2->a = 3;      // CS0214  
      s.a = 0;  
   }  
  
   // OK  
   unsafe public static void Test2()  
   {  
      S s = new S();  
      S * s2 = &s;  
      s2->a = 3;  
      s.a = 0;  
   }  
}  
```