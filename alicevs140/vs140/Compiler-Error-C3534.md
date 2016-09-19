---
title: "Compiler Error C3534"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 41d4328b-8ce3-4a11-bb0c-c96f6af03b01
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3534
a 'new expression' whose type contains 'auto' must have a single initializer expression  
  
 If a [new](../vs140/operator-new---new--.md) expression is used with the `auto` keyword and the default [/Zc:auto](../vs140/-Zc-auto--Deduce-Variable-Type-.md) compiler option, the `new` expression must specify a single initializer.  
  
### To correct this error  
  
1.  Specify a single initializer expression for the `new` operator.  
  
## Example  
 The following example demonstrates C3534. The first declaration does not yield an error because it has a direct initializer (0) whose type is `int`. The second declaration yields an error because it does not have an initializer. In the third declaration, the second use of the `auto` keyword yields an error because the `new` operator does not have an initializer.  
  
```  
// C3534.cpp  
// Compile with /Zc:auto  
int main()  
{  
   new auto(0);   
   new auto();          // C3534  
   auto x = new auto(); // C3534  
   return 0;  
}  
```  
  
## See Also  
 [auto Keyword](../vs140/auto-Keyword.md)   
 [operator new (<new\>)](../vs140/operator-new---new--.md)