---
title: "Compiler Error C3486"
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
ms.assetid: 27d9c644-8bf8-40c5-9d77-c229602c408d
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3486
a parameter for a lambda cannot have a default argument  
  
 You cannot provide a default value for a parameter to a lambda expression.  
  
### To correct this error  
  
-   Remove the default value specification from the parameter.  
  
## Example  
 The following example generates C3486 because it provides a default value for a parameter to a lambda expression:  
  
```  
// C3486.cpp  
  
int main()  
{  
   [](int m, int n = 6) { return m + n; }(1, 3); // C3486  
}  
```  
  
## See Also  
 [Lambda Expressions in C++](../vs140/Lambda-Expressions-in-C--.md)