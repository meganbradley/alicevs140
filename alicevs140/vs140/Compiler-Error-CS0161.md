---
title: "Compiler Error CS0161"
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
ms.assetid: c2731a6c-0285-4558-9e62-a7fd480ab0cf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0161
'method': not all code paths return a value  
  
 A method that returns a value must have a `return` statement in all code paths. For more information, see [Class and Struct Methods (C# Programmer's Reference)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0161:  
  
```  
// CS0161.cs  
public class Test  
{  
   public static int Main() // CS0161  
   {  
      int i = 10;  
      if (i < 10)  
      {  
         return i;  
      }  
      else  
      {  
         // uncomment the following line to resolve  
         // return 1;  
      }  
   }  
}  
```