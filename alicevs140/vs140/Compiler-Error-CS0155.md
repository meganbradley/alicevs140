---
title: "Compiler Error CS0155"
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
ms.assetid: 6c92984a-2b10-453e-9cb7-e6a1d1b98aa6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0155
The type caught or thrown must be derived from System.Exception  
  
 An attempt was made to pass a data type that does not derive from **System.Exception** into a [catch](../Topic/try-catch%20\(C%23%20Reference\).md) block. Only data types that derive from **System.Exception** can be passed into a **catch** block. For more information, see [Exception Handling Statements](../vs140/Exception-Handling-Statements--C#-Reference-.md) and [Exceptions and Exception Handling (C# Programmer's Reference)](../Topic/Exceptions%20and%20Exception%20Handling%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0155:  
  
```  
// CS0155.cs  
using System;  
  
namespace MyNamespace  
{  
    public class MyClass2  
    // try the following line instead  
    // public class MyClass2 : Exception  
    {  
    }  
    public class MyClass  
    {  
        public static void Main()  
        {  
            try  
            {  
            }  
            catch (MyClass2)   // CS0155, resolves if you derive MyClass2 from Exception  
            {  
            }  
        }  
    }  
}  
```