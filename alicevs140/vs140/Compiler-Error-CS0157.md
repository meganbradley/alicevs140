---
title: "Compiler Error CS0157"
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
ms.assetid: a5d9d506-81f8-47dd-85b6-85f8170bcbef
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0157
Control cannot leave the body of a finally clause  
  
 All of the statements in a [finally](../vs140/try-catch-finally--C#-Reference-.md) clause must execute. For more information, see [Exception Handling Statements](../vs140/Exception-Handling-Statements--C#-Reference-.md) and [Exceptions and Exception Handling (C# Programmer's Reference)](../Topic/Exceptions%20and%20Exception%20Handling%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0157:  
  
```  
// CS0157.cs  
using System;  
namespace MyNamespace  
{  
   public class MyClass2 : Exception  
   {  
   }  
  
   public class MyClass  
   {  
      public static void Main()  
      {  
         try  
         {  
         }  
  
         finally  
         {  
            return;   // CS0157, cannot leave finally clause  
         }  
      }  
   }  
}  
```