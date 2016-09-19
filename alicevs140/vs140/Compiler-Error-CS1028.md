---
title: "Compiler Error CS1028"
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
ms.assetid: 9df07db3-256f-45e9-8323-26539c55a1d8
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1028
Unexpected preprocessor directive  
  
 A [preprocessor directive](../vs140/C#-Preprocessor-Directives.md) was found but not expected.  
  
 For example, a `#endif` was found with no preceding `#if`.  
  
 The following sample generates CS1028:  
  
```  
// CS1028.cs  
#endif   // CS1028, no matching #if  
namespace x  
{  
   public class clx  
   {  
      public static void Main()  
      {  
      }  
   }  
}  
```