---
title: "Compiler Warning (level 2) C4396"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7cd6b283-db17-4574-b299-03e0b913ad70
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) C4396
"name" : the inline specifier cannot be used when a friend declaration refers to a specialization of a function template  
  
 A specialization of a function template cannot specify any of the [inline](../vs140/inline--__inline--__forceinline.md) specifiers. The compiler issues warning C4396 and ignores the inline specifier.  
  
### To correct this error  
  
-   Remove the `inline`, `__inline`, or `__forceinline` specifier from the friend function declaration.  
  
## Example  
 The following code example shows an invalid friend function declaration with an `inline` specifier.  
  
```  
// C4396.cpp  
// compile with: /W2 /c  
  
class X;   
template<class T> void Func(T t, int i);  
  
class X {  
    friend inline void Func<char>(char t, int i);  //C4396  
// try the following line instead  
//    friend void Func<char>(char t, int i);   
    int i;  
};  
```