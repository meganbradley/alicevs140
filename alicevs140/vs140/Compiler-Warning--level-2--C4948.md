---
title: "Compiler Warning (level 2) C4948"
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
ms.assetid: d006cb17-754a-4c70-ba7f-c3200e2cd8fa
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) C4948
return type of 'accessor' does not match the last parameter type of the corresponding setter  
  
 The compiler found a mismatch between what data type is being get and set for an indexed property.  
  
 C4948 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C4948:  
  
```  
// C4948.cpp  
// compile with: /clr:oldSyntax /LD /W2  
  
__gc class MyClass  
{  
   int prop __nogc [2];  
   public:  
  
      __property int get_P(int i)  
      // try the following line instead  
      // __property char get_P(int i)  
      {  
         return prop[i];  
      }  
  
      __property void set_P(int i, char c)  
      {  
         prop[i] = c;  
      }  
};   // C4948  
```