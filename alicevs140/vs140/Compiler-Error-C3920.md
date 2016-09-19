---
title: "Compiler Error C3920"
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
ms.assetid: 66e91f28-ed82-4ce2-bf22-c0c74905b1ed
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3920
'operator'' : cannot define a postfix increment/decrement WinRT or CLR operator  Calling the postfix WinRT or CLR operator will call the corresponding prefix WinRT or CLR operator (op_Increment/op_Decrement), but with postfix semantics  
  
 The Windows Runtime and CLR do not support the postfix operator and user-defined postfix operators are not allowed.  You can define a prefix operator and the prefix operator will be used for both pre- and post-increment operations.  
  
 The following sample generates C3920 and shows how to fix it:  
  
```  
// C3920.cpp  
// compile with: /clr /LD  
public value struct V {  
   static V operator ++(V me, int)  
   // try the following line instead  
   // static V operator ++(V me)  
   {   // C3920  
      me.m_i++;  
      return me;  
   }  
  
   int m_i;  
};  
  
```