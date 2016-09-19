---
title: "Compiler Error CS1624"
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
ms.assetid: af7d049d-27e2-4ce1-973c-5c2cb3e56a63
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1624
The body of 'accessor' cannot be an iterator block because 'type' is not an iterator interface type  
  
 This error occurs if an iterator accessor is used but the return type is not one of the iterator interface types: <xref:System.Collections.IEnumerable?qualifyHint=False>, <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>, <xref:System.Collections.IEnumerator?qualifyHint=False>, <xref:System.Collections.Generic.IEnumerator`1?qualifyHint=False>. To avoid this error, use one of the iterator interface types as a return type.  
  
## Example  
 The following sample generates CS1624:  
  
```  
// CS1624.cs  
using System;  
using System.Collections;  
  
class C  
{  
    public int Iterator  
    // Try this instead:  
    // public IEnumerable Iterator  
    {  
        get  // CS1624  
        {  
            yield return 1;  
        }  
    }  
}  
```