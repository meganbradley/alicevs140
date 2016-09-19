---
title: "Compiler Warning (level 1) CS1720"
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
ms.assetid: 97adc294-3a4c-4418-a4ed-ccff43125b62
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1720
Expression will always cause a System.NullReferenceException because the default value of 'generic type' is null  
  
 If you write an expression involving the default of a generic type variable that is a reference type (for example, a class), this error will occur. Consider the following expression:  
  
```  
default(T).ToString()  
```  
  
 Since `T` is a reference type, its default value is null, and so attempting to apply the <xref:System.Object.ToString?qualifyHint=False> method to it will throw a <xref:System.NullReferenceException?qualifyHint=False>.  
  
## Example  
 The class reference constraint on type `T` ensures that `T` is a reference type.  
  
 The following sample generates CS1720.  
  
```  
// CS1720.cs  
using System;  
public class Tester   
{  
    public static void GenericClass<T>(T t1) where T : class   
    {  
        Console.WriteLine(default(T).ToString());  // CS1720  
    }  
    public static void Main() {}  
}  
```