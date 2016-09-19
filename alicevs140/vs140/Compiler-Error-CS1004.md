---
title: "Compiler Error CS1004"
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
ms.assetid: 93cc1b93-ca4c-49a8-af03-9fbfc84ccab9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1004
Duplicate 'modifier' modifier  
  
 A duplicate modifier, such as an **access** modifier, was detected.  
  
 The following sample generates CS1004:  
  
```  
// CS1004.cs  
public class clx  
{  
   public public static void Main()   // CS1004, two public keywords  
   {  
   }  
}  
```