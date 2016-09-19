---
title: "Compiler Error CS0017"
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
ms.assetid: 5e2a3eb3-6f6e-485d-8293-ceabea4d6905
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0017
Program 'output file name' has more than one entry point defined. Compile with /main to specify the type that contains the entry point.  
  
 A program can only have one [Main](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md) method.  
  
 To resolve this error, you can either delete all Main methods in your code, except one, or you can use the [/main](../Topic/-main%20\(C%23%20Compiler%20Options\).md) compiler option to specify which Main method you want to use.  
  
 The following sample generates CS0017:  
  
```  
// CS0017.cs  
// compile with: /target:exe  
public class clx  
{  
   static public void Main()  
   {  
   }  
}  
  
public class cly  
{  
   public static void Main()   // CS0017, delete one Main or use /main  
   {  
   }  
}  
```