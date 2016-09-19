---
title: "Compiler Error CS0563"
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
ms.assetid: c1561e4e-7f00-41ff-abff-b8228aee66a4
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0563
One of the parameters of a binary operator must be the containing type  
  
 The method declaration for an [operator overload](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md) must follow certain guidelines.  
  
## Example  
 The following sample generates CS0563:  
  
```  
// CS0563.cs  
public class iii  
{  
    public static implicit operator int(iii x)  
    {  
        return 0;  
    }  
    public static implicit operator iii(int x)  
    {  
        return null;  
    }  
    public static int operator +(int aa, int bb)   // CS0563   
    // Use the following line instead:  
    // public static int operator +(int aa, iii bb)      
    {  
        return 0;  
    }  
    public static void Main()  
    {  
    }  
}  
```