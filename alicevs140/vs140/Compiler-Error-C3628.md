---
title: "Compiler Error C3628"
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
ms.assetid: 0ff5a4a4-fcc9-47a0-a4d8-8af9cf2815f6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3628
'base class' : managed or WinRTclasses only support public inheritance  
  
 An attempt was made to use a managed or WinRT class as a [private](../vs140/private--C---.md) or [protected](../vs140/protected--C---.md) base class. A managed or WinRT class can only be used as a base class with [public](../vs140/public--C---.md) access.  
  
 The following sample generates C3628 and shows how to fix it:  
  
```  
// C3628a.cpp  
// compile with: /clr  
ref class B {  
};  
  
ref class D : private B {   // C3628  
  
// The following line resolves the error.  
// ref class D : public B {  
};  
  
int main() {  
}  
```  
  
 The following sample generates C3628 and shows how to fix it:  
  
```  
// C3628b.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
__gc class B {  
};  
  
__gc class D : B {   // C3628, private is the default access level  
  
// The following line resolves the error.  
// __gc class D : public B {  
};  
  
int main() {  
}  
```