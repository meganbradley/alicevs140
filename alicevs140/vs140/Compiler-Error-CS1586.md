---
title: "Compiler Error CS1586"
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
ms.assetid: 408a4495-6fe6-4e95-a49f-a4d041675fff
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1586
Array creation must have array size or array initializer  
  
 An array was declared incorrectly.  
  
 The following sample generates CS1586:  
  
```  
// CS1586.cs  
using System;  
class MyClass  
{  
   public static void Main()  
   {  
      int[] a = new int[];   // CS1586  
      // try the following line instead  
      int[] b = new int[5];  
   }  
}  
```  
  
## See Also  
 [Arrays (C# Programming Guide)](../Topic/Arrays%20\(C%23%20Programming%20Guide\).md)