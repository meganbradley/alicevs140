---
title: "Compiler Error CS0463"
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
ms.assetid: 0cb4be4e-86ea-4ade-8817-b17d4cacd4d5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0463
Evaluation of the decimal constant expression failed with error: 'error'  
  
 This errors occurs when a constant decimal expression overflows at compile time.  
  
 Typically you get overflow errors at run time. In this case, you defined the constant expression in such a way that the compiler could evaluate the result and know that an overflow would happen.  
  
## Example  
 The following code generates error CS0463.  
  
```  
// CS0463.cs   
using System;   
class MyClass   
{  
    public static void Main()      
    {  
        const decimal myDec = 79000000000000000000000000000.0m + 79000000000000000000000000000.0m; // CS0463  
        Console.WriteLine(myDec.ToString());  
    }  
}  
```