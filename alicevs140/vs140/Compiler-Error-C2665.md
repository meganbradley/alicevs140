---
title: "Compiler Error C2665"
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
ms.assetid: a7f99b61-2eae-4f2b-ba75-ea68fd1e8312
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2665
'function' : none of the number1 overloads can convert parameter number2 from type 'type'  
  
 A parameter of the overloaded function cannot be converted to the required type.  Possible resolutions:  
  
-   Supply a conversion operator.  
  
-   Use explicit conversion.  
  
## Example  
 The following sample generates C2665.  
  
```  
// C2665.cpp  
void func(short, char*){}  
void func(char*, char*){}  
  
int main() {  
   func(0, 1);   // C2665  
   func((short)0, (char*)1);   // OK  
}  
```