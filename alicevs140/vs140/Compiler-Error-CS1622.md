---
title: "Compiler Error CS1622"
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
ms.assetid: 6b53a777-4cd8-423a-84ff-22ff588044d3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1622
Cannot return a value from an iterator. Use the yield return statement to return a value, or yield break to end the iteration.  
  
 An iterator is a special function that returns a value via the yield statement rather than the return statement. For more information, see **iterators**.  
  
 The following sample generates CS1622:  
  
```  
// CS1622.cs  
// compile with: /target:library  
using System.Collections;  
  
class C : IEnumerable  
{  
   public IEnumerator GetEnumerator()  
   {  
      return (IEnumerator) this;  // CS1622  
      yield return this;   // OK  
   }  
}  
```