---
title: "Compiler Error C2950"
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
ms.assetid: 0c471d4d-f5df-489e-9242-486d30639314
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2950
'type' : cannot explicitly instantiate an explicit specialization  
  
 The compiler found an invalid explicit instantiation.  
  
 The following sample generates C2950:  
  
```  
// C2950.cpp  
// compile with: /c  
template <class T>  
struct s;  
  
template <>  
struct s<int> {};  
  
template struct s<int>;   // C2950 delete this instantiation  
```