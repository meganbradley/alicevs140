---
title: "Compiler Error C3495"
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
ms.assetid: 1fd40cb8-8373-403d-b8a8-f08424a50807
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3495
'var': a lambda capture must have automatic storage duration  
  
 You cannot capture a variable that does not have automatic storage duration, such as a variable that is marked `static` or `extern`.  
  
### To correct this error  
  
-   Do not pass a `static` or `extern` variable to the capture list of the lambda expression.  
  
## Example  
 The following example generates C3495 because the `static` variable `n` appears in the capture list of a lambda expression:  
  
```  
// C3495.cpp  
  
int main()  
{  
   static int n = 66;  
   [&n]() { return n; }(); // C3495  
}  
```  
  
## See Also  
 [Lambda Expressions in C++](../vs140/Lambda-Expressions-in-C--.md)   
 [(NOTINBUILD)Storage-Class Specifiers](assetId:///10b3d22d-cb40-450b-994b-08cf9a211b6c)