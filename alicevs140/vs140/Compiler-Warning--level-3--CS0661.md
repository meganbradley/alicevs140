---
title: "Compiler Warning (level 3) CS0661"
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
ms.assetid: c218665e-5947-40bb-b633-d268483e6522
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) CS0661
'class' defines operator == or operator != but does not override Object.GetHashCode()  
  
 The compiler detected the user-defined equality or inequality operator, but no override for the **GetHashCode** function. A user-defined equality or inequality operator implies that you also want to override the **GetHashCode** function.  
  
 The following sample generates CS0661:  
  
```  
// CS0661.cs  
// compile with: /W:3  
class Test   // CS0661  
{  
   public static bool operator == (object o, Test t)  
   {  
      return true;  
   }  
  
   public static bool operator != (object o, Test t)  
   {  
      return true;  
   }  
  
   public override bool Equals(object o)  
   {  
      return true;  
   }  
  
   // uncomment the GetHashCode function to resolve  
   // public override int GetHashCode()  
   // {  
   //    return 0;  
   // }  
  
   public static void Main()  
   {  
   }  
}  
```