---
title: "Compiler Warning (level 2) CS0251"
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
ms.assetid: 791a325a-096d-4d87-b31d-d9b3124210c8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0251
Indexing an array with a negative index (array indices always start at zero)  
  
 Do not use a negative number to index into an array.  
  
 The following sample generates CS0251:  
  
```  
// CS0251.cs  
// compile with: /W:2  
class MyClass  
{  
   public static void Main()  
   {  
      int[] myarray = new int[] {1,2,3};     
      try  
      {  
         myarray[-1]++;   // CS0251  
         // try the following line instead  
         // myarray[1]++;  
      }  
      catch (System.IndexOutOfRangeException e)  
      {  
         System.Console.WriteLine("{0}", e);  
      }  
   }  
}  
```