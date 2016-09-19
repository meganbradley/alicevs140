---
title: "Compiler Warning (level 2) CS0253"
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
ms.assetid: e02d5dac-c2d9-45ca-9dd3-dda06c96f4d6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0253
Possible unintended reference comparison; to get a value comparison, cast the right hand side to type 'type'  
  
 The compiler is doing a reference comparison. If you want to compare the value of strings, cast the right side of the expression to `type`.  
  
 The following sample generates CS0253:  
  
```  
// CS0253.cs  
// compile with: /W:2  
using System;  
class MyClass  
{  
   public static void Main()  
   {  
      string s = "11";  
      object o = s + s;  
  
      bool c = s == o;   // CS0253  
      // try the following line instead  
      // bool c = s == (string)o;  
   }  
}  
```