---
title: "Compiler Error C2396"
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
ms.assetid: 1b515ef6-7af4-400f-b4ed-564313ea15f6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2396
'your_type::operator'type'' : CLR or WinRT user-defined conversion functionnot valid. Must either convert from or convert to: 'T^', 'T^%', 'T^&', where T = 'your_type'  
  
 A conversion function in a Windows Runtime or managed type did not have at least one parameter whose type is the same as the type containing the conversion function.  
  
 The following sample generates C2396 and shows how to fix it:  
  
```  
// C2396.cpp  
// compile with: /clr /c  
  
ref struct Y {  
   static operator int(char c);   // C2396  
  
   // OK  
   static operator int(Y^ hY);  
   // or  
   static operator Y^(char c);  
};  
```