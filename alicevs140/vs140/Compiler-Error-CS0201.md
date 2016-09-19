---
title: "Compiler Error CS0201"
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
ms.assetid: cf5d6701-50cc-4e4f-878b-e1a4ad8a2061
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0201
Only assignment, call, increment, decrement, and new object expressions can be used as a statement  
  
 The compiler generates an error when it encounters an invalid statement. An invalid statement is any line or series of lines ending in a semicolon that does not represent an assignment ([=](../vs140/=-Operator--C#-Reference-.md)), method call [()](../vs140/---Operator--C#-Reference-.md), [new](../vs140/new--C#-Reference-.md), [--](../Topic/--%20Operator%20\(C%23%20Reference\).md) or [++](../vs140/---Operator--C#-Reference-.md) operation. For more information, see [Statements, Expressions, and Operators (C# Programming Guide)](../vs140/Statements--Expressions--and-Operators--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0201 because 2 * 3 is an expression, not a statement. To make the code compile, try assigning the value of the expression to a  variable.  
  
```  
// CS0201.cs  
public class MainClass  
{  
   public static void Main()  
   {  
      2 * 3;   // CS0201  
      // Try the following line instead.  
      //   int i = 2 * 3;  
   }  
}  
```  
  
## Example  
 The following sample generates CS0201 because checked by itself is not a statement, even though it is parameterized by an increment operation.  
  
```  
// CS0201_b.cs  
// compile with: /target:library  
public class MyList<T>   
{  
   public void Add(T x)  
   {  
      int i = 0;  
      if ( (object)x == null)  
      {  
         checked(i++);   // CS0201  
  
         // OK  
         checked {  
            i++;   
         }  
      }  
   }  
}  
```  
  
## See Also  
 [C# Compiler Errors](../vs140/C#-Compiler-Errors.md)