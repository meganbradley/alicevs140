---
title: "Compiler Error C2691"
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
ms.assetid: 6925f8f3-ea60-4909-91e6-b781492c645d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2691
'data type' : a managed or WinRTarray cannot have this element type  
  
 The type of a managed or WinRT array element can be a value type or a reference type.  
  
 The following sample generates C2691:  
  
```  
// C2691a.cpp  
// compile with: /clr  
class A {};  
  
int main() {  
   array<A>^ a1 = gcnew array<A>(20);   // C2691  
   array<int>^ a2 = gcnew array<int>(20);   // value type OK  
}  
```  
  
 The following sample generates C2691:  
  
```  
// C2691b.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
int main() {  
   int * a1 __gc[];   // C2691  
   int * a1 = new int [20];   // OK  
}  
```  
  
 C2691 can also occur if you attempt to define a jagged array using Managed Extensions for C++.  Jagged arrays are supported in the current syntax, see [array](../vs140/Arrays--C---Component-Extensions-.md) for more information.  
  
 The following sample generates C2691:  
  
```  
// C2691c.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
int main() {  
   Int32 myJaggedArray[][] = new Int32 [50][];   // C2691  
}  
```