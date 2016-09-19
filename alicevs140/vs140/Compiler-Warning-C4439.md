---
title: "Compiler Warning C4439"
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
ms.assetid: 9449958f-f407-4824-829b-9e092f2af97d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning C4439
'function' : function definition with a managed type in the signature must have a __clrcall calling convention  
  
 The compiler implicitly replaced a calling convention with [__clrcall](../Topic/__clrcall.md). To resolve this warning, remove the `__cdecl` or `__stdcall` calling convention.  
  
 C4439 is always issued as an error. You can turn off this warning with the `#pragma warning` or **/wd**; see [warning](../vs140/warning.md) or [/w, /Wn, /WX, /Wall, /wln, /wdn, /wen, /won (Warning Level)](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md) for more information.  
  
## Example  
 The following sample generates C4439.  
  
```  
// C4439.cpp  
// compile with: /clr  
void __stdcall f( System::String^ arg ) {}   // C4439  
void __clrcall f2( System::String^ arg ) {}   // OK  
void f3( System::String^ arg ) {}   // OK  
```