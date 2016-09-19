---
title: "Compiler Error CS0056"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8878b09c-5b7b-40e0-be0d-61ef5b36c151
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0056
Inconsistent accessibility: return type 'type' is less accessible than operator 'operator'  
  
 A public construct must return a publicly accessible object. For more information, see [Access Modifiers (C# Programmer's Reference)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0056:  
  
```  
// CS0056.cs  
class MyClass  
// try the following line instead  
// public class MyClass  
{  
}  
  
public class A  
{  
   public static implicit operator MyClass(A a)   // CS0056  
   {  
      return new MyClass();  
   }  
  
   public static void Main()  
   {  
   }  
}  
```