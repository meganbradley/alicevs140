---
title: "Compiler Error CS0218"
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
ms.assetid: f675e06a-c55c-44a1-b5db-0df178fd8f79
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0218
The type ('type') must contain declarations of operator true and operator false  
  
 If you define an operator for a user-defined type, and then try to use the operator as a short-circuit operator, the user-defined operator must have operator true and operator false defined. For more information on short-circuit operators, see [&& Operator](../vs140/---Operator--C#-Reference-.md) and [&#124;&#124; Operator](../vs140/---Operator--C#-Reference-.md).  
  
 The following sample generates CS0218:  
  
```  
// CS0218.cs  
using System;  
public class MyClass  
{  
   // uncomment these operator declarations to resolve this CS0218  
   /*  
   public static bool operator true (MyClass f)  
   {  
      return false;  
   }  
  
   public static bool operator false (MyClass f)  
   {  
      return false;  
   }  
   */  
  
   public static implicit operator int(MyClass x)  
   {  
      return 0;  
   }  
  
   public static MyClass operator & (MyClass f1, MyClass f2)  
   {  
      return new MyClass();  
   }  
  
   public static void Main()  
   {  
      MyClass f = new MyClass();  
      int i = f && f;   // CS0218, requires operators true and false  
   }  
}  
```  
  
## See Also  
 [Conversion Operators (C# Programmer's Reference)](../Topic/Conversion%20Operators%20\(C%23%20Programming%20Guide\).md)