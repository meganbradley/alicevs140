---
title: "Compiler Error CS1627"
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
ms.assetid: 58dd6e22-e9ed-4e5c-ae04-ce255f07064e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1627
Expression expected after yield return  
  
 This error occurs if `yield` is used without an expression. To avoid this error, insert the appropriate expression in the statement.  
  
 The following sample generates CS1627:  
  
```  
// CS1627.cs  
using System.Collections;  
  
class C : IEnumerable  
{  
   public IEnumerator GetEnumerator()  
   {  
      yield return;   // CS1627  
      // To resolve, add the following line:  
      // yield return 0;  
   }  
}  
  
public class CMain  
{  
   public static void Main() { }  
}  
```