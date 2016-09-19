---
title: "Compiler Error CS0123"
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
ms.assetid: 57be2c58-6d87-40af-9376-cd7f91023044
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0123
No overload for 'method' matches delegate 'delegate'  
  
 An attempt to create a delegate failed because the correct signature was not used. Instances of a delegate must be declared with the same signature as the delegate declaration.  
  
 You can resolve this error by adjusting either the method or delegate signature. For more information, see [Delegates (C# Programmer's Reference)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0123.  
  
```  
// CS0123.cs  
delegate void D();  
delegate void D2(int i);  
  
public class C  
{  
   public static void f(int i) {}  
  
   public static void Main()  
   {  
      D d = new D(f);   // CS0123  
      D2 d2 = new D2(f);   // OK  
   }  
}  
```