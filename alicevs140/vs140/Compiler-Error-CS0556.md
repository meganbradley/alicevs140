---
title: "Compiler Error CS0556"
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
ms.assetid: e2430c6e-784f-4ab2-88b9-f660d956e9e8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0556
User-defined conversion must convert to or from the enclosing type  
  
 A user-defined conversion routine must convert to or from the class that contains the routine.  
  
 The following sample generates CS0556:  
  
```  
// CS0556.cs  
namespace x  
{  
   public class ii  
   {  
      public class iii  
      {  
         public static implicit operator int(byte aa)   // CS0556  
         // try the following line instead  
         // public static implicit operator int(iii aa)  
         {  
            return 0;  
         }  
      }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```