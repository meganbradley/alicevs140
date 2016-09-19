---
title: "Compiler Error CS0242"
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
ms.assetid: bc86a5a4-89c1-4de4-a874-4dd4cbf592c2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0242
The operation in question is undefined on void pointers  
  
 Incrementing a void pointer is not allowed. For more information, see [Unsafe Code and Pointers (C# Programmer's Reference)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md).  
  
 The following sample generates CS0242:  
  
```  
// CS0242.cs  
// compile with: /unsafe  
class TestClass  
{  
   public unsafe void Test()  
   {  
      void * p = null;  
      p++;   // CS0242, incrementing a void pointer not allowed  
   }  
  
   public static void Main()  
   {  
   }  
}  
```