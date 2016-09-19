---
title: "Compiler Error C2217"
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
ms.assetid: 1ce1e3f5-4171-4376-804d-967f7e612935
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2217
'attribute1' requires 'attribute2'  
  
 The first function attribute requires the second attribute.  
  
### To fix by checking the following possible causes  
  
1.  Interrupt (`__interrupt`) function declared as `near`. Interrupt functions must be `far`.  
  
2.  Interrupt function declared with `__stdcall`, or `__fastcall`. Interrupt functions must use C calling conventions.  
  
## Example  
 C2217 can also occur if you attempt to bind a delegate to a CLR function that takes a variable number of arguments. If the function also has e param array overload, use that instead. The following sample generates C2217.  
  
```  
// C2217.cpp  
// compile with: /clr  
using namespace System;  
delegate void MyDel(String^, Object^, Object^, ...);   // C2217  
delegate void MyDel2(String ^, array<Object ^> ^);   // OK  
  
int main() {  
   MyDel2^ wl = gcnew MyDel2(Console::WriteLine);  
   array<Object ^ > ^ x = gcnew array<Object ^>(2);  
   x[0] = safe_cast<Object^>(0);  
   x[1] = safe_cast<Object^>(1);  
  
   // wl("{0}, {1}", 0, 1);  
   wl("{0}, {1}", x);  
}  
```