---
title: "Compiler Error C3734"
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
ms.assetid: 4e2afdcc-7da9-45a1-9c96-85f25e2986e8
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3734
'class': a managed or WinRT class cannot be a coclass  
  
 The [coclass](../vs140/coclass.md) attribute cannot be used with managed or WinRT classes.  
  
 The following sample generates C3734 and shows how to fix it:  
  
```  
// C3734.cpp  
// compile with: /clr /c  
[module(name="x")];  
  
[coclass]  
ref class CMyClass {   // C3734 remove the ref keyword to resolve  
};  
```  
  
 The following sample generates C3734 and shows how to fix it:  
  
```  
// C3734_b.cpp  
// compile with: /clr:oldSyntax /c  
[module(name="x")];  
  
[coclass]  
__gc class CMyClass {   // C3734 remove the __gc keyword to resolve  
};  
```