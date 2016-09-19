---
title: "Compiler Warning (level 2) CS0252"
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
ms.assetid: ff82fbac-01cf-4ae9-b6a0-3aa990096b46
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0252
Possible unintended reference comparison; to get a value comparison, cast the left hand side to type 'type'  
  
 The compiler is doing a reference comparison. If you want to compare the value of strings, cast the left side of the expression to `type`.  
  
 The following sample generates CS0252:  
  
```  
// CS0252.cs  
// compile with: /W:2  
using System;  
  
class MyClass  
{  
   public static void Main()  
   {  
      string s = "11";  
      object o = s + s;  
  
      bool b = o == s;   // CS0252  
      // try the following line instead  
      // bool b = (string)o == s;  
   }  
}  
```