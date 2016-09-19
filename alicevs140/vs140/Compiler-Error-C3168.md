---
title: "Compiler Error C3168"
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
ms.assetid: 4c36fcfb-c351-48ff-b4eb-78d2aa1b4d55
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3168
'type' : illegal underlying type for enum  
  
 The underlying type you specified for the `enum` type was not valid. The underlying type must be an integral C++ type or a corresponding CLR type.  
  
 The following sample generates C3168:  
  
```  
// C3168.cpp  
// compile with: /clr /c  
ref class G{};  
  
enum class E : G { e };   // C3168  
enum class F { f };   // OK  
```  
  
 The following sample generates C3168:  
  
```  
// C3168_2.cpp  
// compile with: /clr:oldSyntax /c  
__gc class G {};  
  
__value enum E : G {e};   // C3168  
__value enum F {f};   // OK  
```