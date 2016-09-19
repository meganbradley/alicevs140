---
title: "Compiler Error CS0131"
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
ms.assetid: 822852cc-a426-4b7d-b2ff-0026a0c0a0e7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0131
The left-hand side of an assignment must be a variable, property or indexer  
  
 In an assignment statement, the value of the right-hand side is assigned to the left-hand side. The left-hand side must be a variable, property, or indexer.  
  
 To fix this error, make sure that all operators are on the right-hand side and that the left-hand side is a variable, property, or indexer. For more information, see [Statements, Expressions, and Operators (C# Programmers Reference)](../vs140/Statements--Expressions--and-Operators--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0131.  
  
```  
// CS0131.cs  
public class MyClass  
{  
    public int i = 0;  
    public void MyMethod()  
    {  
        i++ = 1;   // CS0131  
        // try the following line instead  
        // i = 1;  
    }  
    public static void Main() { }  
}  
```  
  
## Example  
 This error can also occur if you attempt to perform arithmetic operations on the left hand side of an assignment operator, as in the following example.  
  
```  
// CS0131b.cs  
public class C  
{  
    public static int Main()  
    {  
        int a = 1, b = 2, c = 3;  
        if (a + b = c) // CS0131  
        // try this instead  
        // if (a + b == c)  
            return 0;  
        return 1;  
    }  
}  
```