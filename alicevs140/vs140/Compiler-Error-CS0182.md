---
title: "Compiler Error CS0182"
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
ms.assetid: a9e97bb8-f06e-499f-aadf-26abc2082f98
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0182
An attribute argument must be a constant expression, typeof expression or array creation expression of an attribute parameter type  
  
 Certain restrictions apply to what kinds of arguments may be used with attributes. Note that in addition to the restrictions specified in the error message, the following types are NOT allowed as attribute arguments:  
  
-   [sbyte](../Topic/sbyte%20\(C%23%20Reference\).md)  
  
-   [ushort](../Topic/ushort%20\(C%23%20Reference\).md)  
  
-   [uint](../Topic/uint%20\(C%23%20Reference\).md)  
  
-   [ulong](../Topic/ulong%20\(C%23%20Reference\).md)  
  
-   [decimal](../Topic/decimal%20\(C%23%20Reference\).md)  
  
 For more information, see [NOT IN BUILD: Global Attributes (C# Programming Guide)](assetId:///7c6c41f8-f0d5-4345-8987-3d91f9bae136).  
  
## Example  
 The following sample generates CS0182:  
  
```  
// CS0182.cs  
public class MyClass  
{  
    static string s = "Test";  
  
    [System.Diagnostics.ConditionalAttribute(s)]   // CS0182  
    // try the following line instead  
    // [System.Diagnostics.ConditionalAttribute("Test")]  
    void NonConstantArgumentToConditional()  
    {  
    }  
  
    public static void Main()  
    {  
    }  
}  
```