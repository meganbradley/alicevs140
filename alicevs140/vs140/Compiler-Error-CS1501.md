---
title: "Compiler Error CS1501"
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
ms.topic: error-reference
ms.assetid: 99a59646-e2c8-4ee5-9785-4a2c1ae77458
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1501
No overload for method 'method' takes 'number' arguments  
  
 A call was made to a class method, but no definition of the method takes the specified number of arguments.  
  
## Example  
 The following sample generates CS1501.  
  
```c#  
using System;  
  
namespace ConsoleApplication1  
{  
    class Program  
    {  
        static void Main(string[] args)  
        {  
            ExampleClass ec = new ExampleClass();  
            ec.ExampleMethod();  
            ec.ExampleMethod(10);  
            // The following line causes compiler error CS1501 because   
            // ExampleClass does not contain an ExampleMethod that takes  
            // two arguments.  
            ec.ExampleMethod(10, 20);  
        }  
    }  
  
    // ExampleClass contains two overloads for ExampleMethod. One of them   
    // has no parameters and one has a single parameter.  
    class ExampleClass  
    {  
        public void ExampleMethod()  
        {  
            Console.WriteLine("Zero parameters");  
        }  
  
        public void ExampleMethod(int i)  
        {  
            Console.WriteLine("One integer parameter.");  
        }  
  
        //// To fix the error, you must add a method that takes two arguments.  
        //public void ExampleMethod (int i, int j)  
        //{  
        //    Console.WriteLine("Two integer parameters.");  
        //}  
    }  
}  
```