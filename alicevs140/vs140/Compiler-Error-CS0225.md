---
title: "Compiler Error CS0225"
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
ms.assetid: 0b0cd72b-c47a-44d1-9b27-d1a1fad06807
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0225
The params parameter must be a single dimensional array  
  
 When using the [params](../vs140/params--C#-Reference-.md) keyword, you must specify a single-dimensional array of the data type. For more information, see [Class and Struct Methods (C# Programmer's Reference)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0225:  
  
```  
// CS0225.cs  
public class MyClass  
{  
    public static void TestParams(params int a)   // CS0225  
    // try the following line instead  
    // public static void TestParams(params int[] a)  
    {  
    }  
  
    public static void Main()  
    {  
        TestParams(1);  
    }  
}  
```