---
title: "Compiler Error CS0055"
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
ms.assetid: 4d98abf3-2690-4418-8fd0-50c0e67d0a4a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0055
Inconsistent accessibility: parameter type 'type' is less accessible than indexer 'indexer'  
  
 A public construct must return a publicly accessible object. For more information, see [Access Modifiers (C# Programmer's Reference)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0055:  
  
```  
// CS0055.cs  
class MyClass //defaults to private accessibility  
// try the following line instead  
// public class MyClass  
{  
}  
  
public class MyClass2  
{  
   public int this[MyClass myClass]   // CS0055  
   {  
      get  
      {  
         return 0;  
      }  
   }  
}  
  
public class MyClass3  
{  
   public static void Main()  
   {  
   }  
}  
```