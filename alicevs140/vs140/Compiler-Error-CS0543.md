---
title: "Compiler Error CS0543"
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
ms.assetid: f85e09a7-0e08-4dea-8f64-218c0876e4f6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0543
'enumeration' : the enumerator value is too large to fit in its type  
  
 A value that was assigned to an element in an [enumeration](../Topic/enum%20\(C%23%20Reference\).md) is outside the range of the data type.  
  
 The following sample generates CS0543:  
  
```  
// CS0543.cs  
namespace x  
{  
   enum I : byte  
   {a = 255, b, c}   // CS0543  
   public class clx  
   {  
      public static int Main()  
      {  
         return 0;  
      }  
   }  
}  
```