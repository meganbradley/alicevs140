---
title: "Compiler Error C2846"
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
ms.assetid: bc090ec2-5410-4112-9ec6-261325374375
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2846
'constructor' : an interface cannot have a constructor  
  
 A Visual C++ [interface](../vs140/__interface.md) cannot have a constructor.  
  
 The following sample generates C2846:  
  
```  
// C2846.cpp  
// compile with: /c  
__interface C {  
   C();   // C2846 constructor not allowed in an interface  
};  
```