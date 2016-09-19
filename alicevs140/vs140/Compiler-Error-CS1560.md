---
title: "Compiler Error CS1560"
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
ms.assetid: 772c4543-6c8d-453f-ae3f-d333528eb8b3
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1560
Invalid filename specified for preprocessor directive. Filename is too long or not a valid filename  
  
 The file name that was specified with [#line](../vs140/#line--C#-Reference-.md) exceeded _MAX_PATH (256 characters) or the line on which `#line` was found exceeded 2000 characters.  
  
## Example  
 The following sample generates CS1560.  
  
```  
// cs1560.cs   
using System;   
class MyClass   
{     
   public static void Main()      
   {        
      Console.WriteLine("Normal line #1.");     
      #line 21 "MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890MyFile1234567890.txt"   // CS1560  
    }  
}  
```