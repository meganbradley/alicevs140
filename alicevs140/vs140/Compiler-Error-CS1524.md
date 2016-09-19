---
title: "Compiler Error CS1524"
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
ms.assetid: a7b80bbc-a2de-4718-b0f0-4c9526726525
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1524
Expected catch or finally  
  
 A `try` block must be followed by a `catch` or `finally` block.  
  
 For more information on exceptions, see [Exception Handling Statements](../vs140/Exception-Handling-Statements--C#-Reference-.md).  
  
## Example  
 The following sample generates CS1524:  
  
```  
// CS1524.cs  
class x  
{  
    public static void Main()  
    {  
        try  
        {  
            // Code here  
        }  
        catch  
        {  
        }  
        try  
        {  
            // Code here  
        }  
        finally  
        {  
        }  
        try  
        {  
            // Code here  
        }  
    }     // CS1524, missing catch or finally  
}  
```