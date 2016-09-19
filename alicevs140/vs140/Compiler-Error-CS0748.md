---
title: "Compiler Error CS0748"
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
ms.assetid: da1935af-a5ea-41f4-84ae-58559b750566
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0748
Inconsistent lambda parameter usage; all parameter types must either be explicit or implicit.  
  
 If a lambda expression has multiple input parameters, some parameters cannot use implicit typing while others use explicit typing.  
  
### To correct this error  
  
1.  Give all the input parameters implicit types, or give them all explicit types.  
  
## Example  
 The following code generates CS0748 because, in the lambda expression, only `alpha` is given an explicit type:  
  
```  
// cs0748.cs  
class CS0748  
{  
    delegate double D(int x, int y);  
    D d = (int alpha, beta) => { return beta / alpha; }; // CS0748  
}  
```  
  
## See Also  
 [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md)