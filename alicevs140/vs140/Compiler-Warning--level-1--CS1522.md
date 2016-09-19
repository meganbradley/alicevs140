---
title: "Compiler Warning (level 1) CS1522"
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
ms.assetid: afb99bbf-a1d9-441e-b392-6845bea23f27
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1522
Empty switch block  
  
 The compiler detected a [switch](../vs140/switch--C#-Reference-.md) block with no **case** or **default** statement. A `switch` block must have one or more **case** or **default** statements.  
  
 The following sample generates CS1522:  
  
```  
// CS1522.cs  
// compile with: /W:1  
using System;  
class x  
{  
   public static void Main()  
   {  
      int i = 6;  
  
      switch(i)   // CS1522  
      {  
         // add something to the switch block, for example:  
         /*  
         case (5):  
            Console.WriteLine("5");  
            return;  
         default:  
            Console.WriteLine("not 5");  
            return;  
         */  
      }  
   }  
}  
```