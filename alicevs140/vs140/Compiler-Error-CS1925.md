---
title: "Compiler Error CS1925"
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
ms.assetid: b60806a5-2ccf-47f5-873b-7ac2292fdb54
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1925
Cannot initialize object of type 'type' with a collection initializer.  
  
 Collection initializers are only allowed for collection classes that meet certain criteria. For more information, see [Object and Collection Initializers (C# Programming Guide)](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md). This error is also produced when you try to use the short form of an array initializer nested inside a collection initializer.  
  
### To correct this error  
  
1.  Initialize the object by calling its constructors and methods.  
  
## Example  
 The following code generates CS1925:  
  
```  
// cs1925.cs  
public class Student  
{  
    public int[] Scores;  
}  
  
class Test  
{  
    static void Main(string[] args)  
    {  
        Student student = new Student { Scores = { 1, 2, 3 } }; // CS1925  
    }  
}  
```