---
title: "Compiler Error C3491"
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
ms.assetid: 7f0e71b2-46a0-4d25-bd09-6158a280f509
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3491
'var': a by-value capture cannot be modified in a non-mutable lambda  
  
 A non-mutable lambda expression cannot modify the value of a variable that is captured by value.  
  
### To correct this error  
  
-   Declare your lambda expression with the `mutable` keyword, or  
  
-   Pass the variable by reference to the capture list of the lambda expression.  
  
## Example  
 The following example generates C3491 because the body of a non-mutable lambda expression modifies the capture variable `m`:  
  
```  
// C3491a.cpp  
  
int main()  
{  
   int m = 55;  
   [m](int n) { m = n; }(99); // C3491  
}  
```  
  
## Example  
 The following example resolves C3491 by declaring the lambda expression with the `mutable` keyword:  
  
```  
// C3491b.cpp  
  
int main()  
{  
   int m = 55;  
   [m](int n) mutable { m = n; }(99);  
}  
```  
  
## See Also  
 [Lambda Expressions in C++](../vs140/Lambda-Expressions-in-C--.md)