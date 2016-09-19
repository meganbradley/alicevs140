---
title: "Compiler Error CS0562"
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
ms.topic: article
ms.assetid: dceecce5-90ce-4554-820c-f4c06b2b8258
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0562
The parameter of a unary operator must be the containing type  
  
 The method declaration for an operator overload must follow certain guidelines. For more information, see [Overloadable Operators](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md) and [Operator Overloading Sample](assetId:///1c6b4610-0a49-4532-8fa7-f694cfc65743).  
  
## Example  
 The following sample generates CS0562:  
  
```  
// CS0562.cs  
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
  
    public static iii operator +(int aa)   // CS0562  
    // try the following line instead  
    // public static iii operator +(iii aa)  
    {  
        return (iii)0;  
    }  
  
    public static void Main()  
    {  
    }  
}  
```