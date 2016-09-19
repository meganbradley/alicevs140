---
title: "Compiler Error CS0450"
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
ms.assetid: 8eb0e98b-d7a1-49a7-8e55-36e2eb0057ff
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0450
'Type Parameter Name': cannot specify both a constraint class and the 'class' or 'struct' constraint  
  
 If a type parameter is constrained by the struct type constraint, it is logically contradictory for it to also be constrained by a specific class type, since struct and class are mutually exclusive categories. If a type parameter is constrained by a specific class type constraint, then it is by definition constrained by the class type constraint, and so specifying the class type constraint is redundant.  
  
## Example  
  
```  
// CS0450.cs  
// compile with: /t:library  
public class GenericsErrors   
{  
    public class B { }  
    public class G3<T> where T : struct, B { } // CS0450  
// To resolve, use the following line instead:  
// public class G3<T> where T : B { }  
}  
```