---
title: "Compiler Error C3483"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 18b3a2c5-dfc9-4661-9653-08a5798474cf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3483
'var' is already part of the lambda capture list  
  
 You passed the same variable to the capture list of a lambda expression more than one time.  
  
### To correct this error  
  
-   Remove all additional instances of the variable from the capture list.  
  
## Example  
 The following example generates C3483 because the variable `n` appears more than one time in the capture list of the lambda expression:  
  
```  
// C3483.cpp  
  
int main()  
{  
   int m = 6, n = 5;  
   [m,n,n] { return n + m; }(); // C3483  
}  
```  
  
## See Also  
 [Lambda Expressions in C++](../vs140/Lambda-Expressions-in-C--.md)