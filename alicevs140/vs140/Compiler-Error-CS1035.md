---
title: "Compiler Error CS1035"
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
ms.assetid: 99125500-62de-421a-b12b-04311c8947c3
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1035
End-of-file found, '*/' expected  
  
 An opening comment delimiter was not matched with a closing delimiter.  
  
 The following sample generates CS1035:  
  
```  
// CS1035.cs  
public class a  
{  
   public static void Main()  
   {  
   }  
}  
/*   // CS1035, needs closing comment  
```