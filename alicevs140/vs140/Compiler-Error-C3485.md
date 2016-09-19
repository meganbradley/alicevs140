---
title: "Compiler Error C3485"
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
ms.assetid: d67536f9-67a1-4ad9-9a94-d8bbbca3d0dc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3485
a lambda definition cannot have any cv-qualifiers  
  
 You cannot use a `const` or `volatile` qualifier as part of the definition of a lambda expression.  
  
### To correct this error  
  
-   Remove the `const` or `volatile` qualifier from the definition of your lambda expression.  
  
## Example  
 The following example generates C3485 because it uses the `const` qualifier as part of the definition of a lambda expression:  
  
```  
// C3485.cpp  
  
int main()  
{  
   auto x = []() const mutable {}; // C3485  
}  
```  
  
## See Also  
 [Lambda Expressions in C++](../vs140/Lambda-Expressions-in-C--.md)