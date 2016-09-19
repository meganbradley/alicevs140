---
title: "Compiler Error C3279"
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
ms.assetid: 639afc20-984c-4a95-be35-8bf9409f02d5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3279
partial and explicit specializations as well as explicit instantiations of class templates declared in the cli namespace are disallowed  
  
 The `cli` namespace is defined by Microsoft and contains pseudo-templates. The Visual C++ compiler does not allow user-defined, partial and explicit specializations, and explicit instantiations of class templates in this namespace.  
  
 The following sample generates C3279:  
  
```  
// C3279.cpp  
// compile with: /clr  
namespace cli {  
   template <> ref class array<int> {};   // C3279  
   template <typename T> ref class array<T, 2> {};   // C3279  
}  
```