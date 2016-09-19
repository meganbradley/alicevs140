---
title: "Compiler Error CS1059"
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
ms.assetid: 3ebd02ab-e40d-4aad-b901-a0cb6e2eace7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1059
The operand of an increment or decrement operator must be a variable, property or indexer.  
  
 This error is raised when you try to increment or decrement a constant value. It can also occur if you try to increment an expression such as `(a+b)++`.  
  
### To correct this error  
  
-   Make the variable non-const.  
  
-   Remove the increment or decrement operator.  
  
-   Store the expression in a variable, and then increment the variable.  
  
## Example  
 The following example generates CS1059 because `i` is a constant, not a variable, and `E` is an `Enum` type, whose elements are also constant values.  
  
```  
// CS1059.cs  
    class Program  
    {  
        public enum E : sbyte  
        {  
            a = 1,  
            b = 2  
        }  
  
        static void Main(string[] args)  
        {  
            const int i = 0;  
            i++;            // CS1059  
            E test = E.a++; // CS1059  
        }  
    }  
```  
  
## See Also  
 [Constants (C# Programming Guide)](../Topic/Constants%20\(C%23%20Programming%20Guide\).md)