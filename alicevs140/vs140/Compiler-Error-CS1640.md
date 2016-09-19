---
title: "Compiler Error CS1640"
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
ms.assetid: 1393668e-05e9-4dc2-9203-3d9c2933406f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1640
foreach statement cannot operate on variables of type 'type' because it implements multiple instantiations of 'interface', try casting to a specific interface instantiation  
  
 The type inherits from two or more instances of IEnumerator<T\>, which means there is not a unique enumeration of the type that `foreach` could use. Specify the type of IEnumerator<T\> or use another looping construct.  
  
## Example  
 The following sample generates CS1640:  
  
```  
// CS1640.cs  
  
using System;  
using System.Collections;  
using System.Collections.Generic;  
  
public class C : IEnumerable, IEnumerable<int>, IEnumerable<string>  
{  
    IEnumerator<int> IEnumerable<int>.GetEnumerator()  
    {  
        yield break;  
    }  
  
    IEnumerator<string> IEnumerable<string>.GetEnumerator()  
    {  
        yield break;  
    }  
  
    IEnumerator IEnumerable.GetEnumerator()  
    {  
        return (IEnumerator)((IEnumerable<string>)this).GetEnumerator();  
    }  
}  
  
public class Test  
{  
    public static int Main()  
    {  
        foreach (int i in new C()){}    // CS1640  
  
        // Try specifing the type of IEnumerable<T>  
        // foreach (int i in (IEnumerable<int>)new C()){}  
        return 1;  
    }  
}  
```