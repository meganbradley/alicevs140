---
title: "Compiler Error C3232"
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
ms.assetid: 3119b3a9-0eff-4a3f-b805-e4d160af9e39
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3232
'param' : a generic type parameter cannot be used in a qualified name  
  
 A generic type parameter was used incorrectly.  
  
 The following sample generates C3232:  
  
```  
// C3232.cpp  
// compile with: /clr  
generic <class T>  
ref class C {  
   typename T::TYPE t;   // C3232  
};  
```