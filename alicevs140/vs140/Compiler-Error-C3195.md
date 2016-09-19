---
title: "Compiler Error C3195"
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
ms.assetid: 97e4f681-812b-49e8-ba57-24b7817e3cd8
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3195
'operator' : is reserved and cannot be used as a member of a ref class or value type. CLR or WinRToperators must be defined using the 'operator' keyword  
  
 The compiler detected an operator definition using the Managed Extensions for C++ syntax.  
  
 Either use the new C++ syntax or use the **/clr:oldSyntax** compiler option to enable the Managed Extensions for C++ syntax.  
  
 The following sample generates C3195 and shows how to fix it:  
  
```  
// C3195.cpp  
// compile with: /clr /LD  
#using <mscorlib.dll>  
value struct V {  
   static V op_Addition(V v, int i);   // C3195  
   static V operator +(V v, char c);   // OK for new C++ syntax   
};  
```