---
title: "Compiler Error CS1625"
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
ms.assetid: 0b25b7f9-a585-49b0-9ee6-4384e87fcea6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1625
Cannot yield in the body of a finally clause  
  
 A yield statement is not allowed in the body of a finally clause. To avoid this error, move the yield statement out of the finally clause.  
  
 The following sample generates CS1625:  
  
```  
// CS1625.cs  
using System.Collections;  
  
class C : IEnumerable  
{  
   public IEnumerator GetEnumerator()  
   {  
      try  
      {  
      }  
      finally  
      {  
        yield return this;  // CS1625  
      }  
   }  
}  
  
public class CMain  
{  
   public static void Main() { }  
}  
  
```