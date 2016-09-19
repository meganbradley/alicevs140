---
title: "Compiler Error C3101"
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
ms.assetid: 4f673766-d4f7-4632-94a5-d36a83f7f4b5
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3101
illegal expression for named attribute argument 'field'  
  
 When initializing a named attribute argument, the value must be a compile time constant.  
  
 For more information on attributes, see [User-Defined Attributes](../Topic/User-Defined%20Attributes%20%20\(C++%20Component%20Extensions\).md).  
  
## Example  
 The following sample generates C3101.  
  
```  
// C3101.cpp  
// compile with: /clr /c  
ref class AAttribute : System::Attribute {  
public:  
   int Field;  
};  
  
extern int i;  
  
[assembly:A(Field = i)];   // C3101  
[assembly:A(Field = 0)];   // OK  
```