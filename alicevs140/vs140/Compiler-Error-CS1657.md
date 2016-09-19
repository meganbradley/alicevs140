---
title: "Compiler Error CS1657"
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
ms.assetid: 6f0aeebe-5c90-4d5b-981c-1795d2e8fbb9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1657
Cannot pass 'parameter' as a ref or out argument because 'reason''  
  
 This error occurs when a variable is passed as a [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md) argument in a context in which that variable is readonly. Readonly contexts include [foreach](../Topic/foreach,%20in%20\(C%23%20Reference\).md) iteration variables, [using](../Topic/using%20Statement%20\(C%23%20Reference\).md) variables, and `fixed` variables. To resolve this error, do not call functions that take the `foreach`, `using` or `fixed` variable as a `ref` or `out` parameter in `using` blocks, `foreach` statements, and `fixed` statements.  
  
## Example  
 The following sample generates CS1657:  
  
```  
// CS1657.cs  
using System;  
class C : IDisposable  
{  
    public int i;  
    public void Dispose() {}  
}  
  
class CMain  
{  
    static void f(ref C c)  
    {  
    }  
    static void Main()  
    {  
        using (C c = new C())  
        {  
            f(ref c);  // CS1657  
        }  
    }  
}  
```  
  
## Example  
 The following code illustrates the same problem in a `fixed` statement:  
  
```  
// CS1657b.cs  
// compile with: /unsafe  
unsafe class C  
{  
    static void F(ref int* p)  
    {  
    }  
  
    static void Main()  
    {  
        int[] a = new int[5];  
        fixed(int* p = a) F(ref p); // CS1657  
    }  
}  
```