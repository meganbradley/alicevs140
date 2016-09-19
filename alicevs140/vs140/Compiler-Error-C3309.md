---
title: "Compiler Error C3309"
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
ms.assetid: 75ee16e3-7d4e-4c41-b3cb-64e9849c3aab
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3309
'macro_name': module name cannot be a macro or a keyword  
  
 The value that you pass to the name property of the module attribute cannot be a symbol for the preprocessor to expand; it must be a string literal.  
  
 The following sample generates C3309:  
  
```  
// C3309.cpp  
#define NAME MyModule  
[module(name="NAME")];   // C3309  
// Try the following line instead  
// [module(name="MyModule")];  
[coclass]  
class MyClass {  
public:  
   void MyFunc();  
};  
  
int main() {  
}  
```