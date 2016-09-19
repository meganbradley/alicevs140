---
title: "Compiler Warning (level 3) C4398"
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
ms.assetid: b6221432-9fed-4272-a547-a73f587904e6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4398
'variable' : per-process global object might not work correctly with multiple appdomains; consider using __declspec(appdomain)  
  
 A virtual function with [__clrcall](../Topic/__clrcall.md) calling convention in a native type causes the creation of a per application domain vtable. Such a variable may not correct correctly when used in multiple application domains.  
  
 You can resolve this warning by compiling with **/clr:pure**, which makes global variables per appdomain by default, or by explicitly marking the variable `__declspec(appdomain)`.  
  
 For more information, see [appdomain](../vs140/appdomain.md) and [Application Domains and Visual C++](../vs140/Application-Domains-and-Visual-C--.md).  
  
## Example  
 The following sample generates C4398.  
  
```  
// C4398.cpp  
// compile with: /clr /W3 /c  
struct S {  
   virtual void f( System::String ^ );   // String^ parameter makes function __clrcall  
};  
  
S glob_s;   // C4398  
__declspec(appdomain) S glob_s2;   // OK  
```