---
title: "Compiler Error CS0163"
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
ms.topic: error-reference
ms.assetid: 00139dcf-33cd-45ea-bf80-d6f26b10a5d2
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0163
Control cannot fall through from one case label ('label') to another  
  
 When a [switch statement](../vs140/switch--C#-Reference-.md) contains more than one switch section, you must explicitly terminate each section, including the last one, by using one of the following keywords:  
  
-   [return](../vs140/return--C#-Reference-.md)  
  
-   [goto](../vs140/goto--C#-Reference-.md)  
  
-   [break](../vs140/break--C#-Reference-.md)  
  
-   [throw](../Topic/throw%20\(C%23%20Reference\).md)  
  
-   [continue](../vs140/continue--C#-Reference-.md)  
  
 If you want to implement "fall through" behavior from one section to the next, use `goto case #`. For more information and examples, see [switch (C# Programmer's Reference)](../vs140/switch--C#-Reference-.md).  
  
 The following sample generates CS0163.  
  
```c#  
// CS0163.cs  
public class MyClass  
{  
    public static void Main()  
    {  
        int i = 0;  
  
        switch (i)   // CS0163  
        {  
            // Compiler error CS0163 is reported on the following line.  
            case 1:  
                i++;  
            // To resolve the error, uncomment one of the following example statements.  
            // return;  
            // break;  
            // goto case 3;  
  
            case 2:  
                i++;  
                return;  
  
            case 3:  
                i = 0;  
                return;  
  
            // Compiler error CS0163 is reported on the following line.  
            default:  
                Console.WriteLine("Default");  
                // To resolve the error, uncomment the following line:  
            //break;  
        }  
    }  
```