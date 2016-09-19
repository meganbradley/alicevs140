---
title: "Compiler Error CS0516"
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
ms.assetid: a9de9d1d-9ee3-4533-ba31-b8cb9f9964a1
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0516
Constructor 'constructor' can not call itself  
  
 A program cannot recursively call constructors.  
  
 The following sample generates CS0516:  
  
```  
// CS0516.cs  
namespace x  
{  
   public class clx  
   {  
      public clx() : this()   // CS0516, delete "this()"  
      {  
      }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```