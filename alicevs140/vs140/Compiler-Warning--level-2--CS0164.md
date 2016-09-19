---
title: "Compiler Warning (level 2) CS0164"
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
ms.assetid: c701265b-ea7d-4d56-ae73-f74e039f1005
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0164
This label has not been referenced  
  
 A label was declared but never used.  
  
 The following sample generates CS0164:  
  
```  
// CS0164.cs  
// compile with: /W:2  
public class a  
{  
   public int i = 0;  
  
   public static void Main()  
   {  
      int i = 0;   // CS0164  
      l1: i++;  
      // the following lines resolve this error  
      // if(i < 10)  
      //    goto l1;  
   }  
}  
```