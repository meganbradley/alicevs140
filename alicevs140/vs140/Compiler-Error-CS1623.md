---
title: "Compiler Error CS1623"
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
ms.assetid: e52bc2d6-5116-40a2-90bc-23a3fa2c73e7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1623
Iterators cannot have ref or out parameters  
  
 This error occurs if an iterator method takes a `ref` or `out` parameter. To avoid this error, remove the `ref` or `out` keyword from the method signature.  
  
## Example  
 The following sample generates CS1623:  
  
```  
// CS1623.cs  
using System.Collections;  
  
class C : IEnumerable  
{  
    public IEnumerator GetEnumerator()  
    {  
        yield return 0;  
    }  
  
    // To resolve the error, remove ref  
    public IEnumerator GetEnumerator(ref int i)  // CS1623  
    {  
        yield return i;  
    }  
  
    // To resolve the error, remove out  
    public IEnumerator GetEnumerator(out float f)  // CS1623  
    {  
        f = 0.0F;  
        yield return f;  
    }  
}  
```