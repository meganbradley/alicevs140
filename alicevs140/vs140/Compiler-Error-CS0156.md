---
title: "Compiler Error CS0156"
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
ms.assetid: 32026b1b-bcd7-4464-b63f-3b38c00452a6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0156
A throw statement with no arguments is not allowed in a finally clause that is nested inside the nearest enclosing catch clause  
  
 A [throw](../Topic/throw%20\(C%23%20Reference\).md) statement with no parameters can only appear in a **catch** clause that takes no parameters.  
  
 For more information, see [Exception Handling Statements](../vs140/Exception-Handling-Statements--C#-Reference-.md) and [Exceptions and Exception Handling (C# Programmer's Reference)](../Topic/Exceptions%20and%20Exception%20Handling%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0156:  
  
```  
// CS0156.cs  
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
            throw;   // CS0156  
         }  
  
         catch(MyClass2)  
         {  
            throw;   // this throw is valid  
         }  
      }  
   }  
}  
```