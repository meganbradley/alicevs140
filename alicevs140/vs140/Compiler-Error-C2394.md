---
title: "Compiler Error C2394"
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
ms.assetid: 653fa9a0-29b3-48aa-bc01-82f98f717a2b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2394
'your_type::operator'op'" : CLR or WinRToperator not valid. At least one parameter must be of the following types: 'T^', 'T^%', 'T^&', where T = 'your_type'  
  
 An operator in a Windows Runtime or managed type did not have at least one parameter whose type is the same as the type of the operator return value.  
  
 The following sample generates C2394:  
  
```  
// C2394.cpp  
// compile with: /clr /c  
ref struct Y {  
   static Y^ operator -(int i, char c);   // C2394  
  
   // OK  
   static Y^ operator -(Y^ hY, char c);  
   // or  
   static Y^ operator -(int i, Y^& rhY);  
};  
```