---
title: "Compiler Error CS0553"
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
ms.assetid: d2d6ddb1-9294-4e85-83d8-c35bd7a70f5b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0553
'conversion routine' : user defined conversion to/from base class  
  
 User-defined conversions to values of a base class are not allowed; you do not need such an operator.  
  
 The following sample generates CS0553:  
  
```  
// CS0553.cs  
namespace x  
{  
   public class ii  
   {  
   }  
  
   public class a : ii  
   {  
      // delete the conversion routine to resolve CS0553  
      public static implicit operator ii(a aa) // CS0553  
      {  
         return new ii();  
      }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```