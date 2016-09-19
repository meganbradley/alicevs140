---
title: "Compiler Error CS0245"
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
ms.assetid: 3f2beb2f-a510-4568-9d11-bb1f65066acd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0245
Destructors and object.Finalize cannot be called directly. Consider calling IDisposable.Dispose if available.  
  
 For more information, see [Programming Essentials for Garbage Collection](assetId:///22b6cb97-0c80-4eeb-a2cf-5ed7655e37f9) and [Destructors (C# Programmer's Reference)](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0245:  
  
```  
// CS0245.cs  
using System;  
using System.Collections;  
  
class MyClass // : IDisposable  
{  
   /*  
   public void Dispose()  
   {  
      // cleanup code goes here  
   }  
   */  
  
   void m()  
   {  
      this.Finalize();   // CS0245  
      // this.Dispose();  
   }  
  
   public static void Main()  
   {  
   }  
}  
```