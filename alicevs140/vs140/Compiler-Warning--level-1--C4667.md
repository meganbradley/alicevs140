---
title: "Compiler Warning (level 1) C4667"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 5d2b7fe0-4f0e-4cd6-b432-ca02c3d194ab
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4667
'function' : no function template defined that matches forced instantiation  
  
 You cannot instantiate a function template that has not been declared.  
  
 The following sample will cause C4667:  
  
```  
// C4667a.cpp  
// compile with: /LD /W1  
template  
void max(const int &, const int &); // C4667 expected  
```  
  
 To avoid this warning, first declare the function template:  
  
```  
// C4667b.cpp  
// compile with: /LD  
// Declare the function template  
template<typename T>  
const T &max(const T &a, const T &b) {  
   return (a > b) ? a : b;  
}  
// Then forcibly instantiate it with a desired type ... i.e. 'int'  
//  
template  
const int &max(const int &, const int &);  
```