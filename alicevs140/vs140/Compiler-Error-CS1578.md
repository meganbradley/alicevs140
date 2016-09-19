---
title: "Compiler Error CS1578"
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
ms.assetid: 8356cd33-5acc-4db7-8bbd-2d25f9d7728e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1578
Filename, single-line comment or end-of-line expected  
  
 After a [#line](../vs140/#line--C#-Reference-.md) directive, only a file name (in double quotation marks) or a single-line comment is allowed.  
  
 The following sample generates CS1578:  
  
```  
// CS1578.cs  
class MyClass  
{  
   static void Main()  
   {  
      #line 101 abc.cs   // CS1578  
      // try the following line instead  
      //#line 101 "abc.cs"  
      intt i;          // error will be reported on line 101  
   }  
}  
```