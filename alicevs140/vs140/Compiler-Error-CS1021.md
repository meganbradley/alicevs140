---
title: "Compiler Error CS1021"
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
ms.assetid: 0346ba58-d7cd-40bd-bcad-b90117fdc9b5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1021
Integral constant is too large  
  
 A value assigned to an [integral type](../vs140/Integral-Types-Table--C#-Reference-.md) is larger than the largest possible unsigned integer value.  
  
 The following sample generates CS1021:  
  
```  
// CS1021.cs  
enum F : int  
{  
   a=(int)2590000000000000000000   // CS1021  
}  
  
public class clx  
{  
   public static void Main()  
   {  
   }  
}  
```