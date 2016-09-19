---
title: "Compiler Warning (level 4) CS0028"
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
ms.assetid: 47df919f-01fa-45ae-a4b7-912445e679e2
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS0028
'function declaration' has the wrong signature to be an entry point  
  
 The method declaration for `Main` was invalid: it was declared with an invalid signature. `Main` must be declared as static and it must return either [int](../Topic/int%20\(C%23%20Reference\).md) or [void](../vs140/void--C#-Reference-.md). For more information, see [Main() and Command-Line Arguments](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0028:  
  
```  
// CS0028.cs  
// compile with: /W:4 /warnaserror  
public class a  
{  
    public static double Main(int i)   // CS0028  
    // Try the following line instead:  
    // public static void Main()  
    {  
    }  
}  
```