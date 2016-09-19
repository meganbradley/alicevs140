---
title: "Compiler Error CS0205"
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
ms.assetid: 616d98cf-e7a5-4f8e-93da-fcd6e1e4de35
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0205
Cannot call an abstract base member: 'method'  
  
 You cannot call an [abstract](../vs140/abstract--C#-Reference-.md) method because it does not have a method body. For more information, see [Abstract and Sealed Classes and Class Members (C# Programmer's Reference)](../vs140/Abstract-and-Sealed-Classes-and-Class-Members--C#-Programming-Guide-.md).  
  
 The following sample generates CS0205:  
  
```  
// CS0205.cs  
abstract public class MyClass  
{  
   abstract public void M();  
}  
  
public class MyClass2 : MyClass  
{  
   public override void M()  
   {  
      base.M();   // CS0205, delete this line  
   }  
  
   public static void Main()  
   {  
   }  
}  
```