---
title: "Compiler Error CS0186"
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
ms.assetid: b8afca3e-0fb9-44c5-b4bb-abe3ef134e85
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0186
Use of null is not valid in this context  
  
 The following sample generates CS0186:  
  
```  
// CS0186.cs  
using System;  
using System.Collections;  
  
class MyClass   
{  
   static void Main()   
   {  
      // Each of the following lines generates CS0186:  
      foreach (int i in null) {}   // CS0186  
      foreach (int i in (IEnumerable) null) { };   // CS0186  
   }  
}  
```