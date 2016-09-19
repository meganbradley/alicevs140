---
title: "Compiler Error C3838"
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
ms.assetid: d6f470c2-131a-4a8c-843a-254acd43da83
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3838
cannot explicitly inherit from 'type'  
  
 The specified `type` cannot act as a base class in any class.  
  
 The following sample generates C3838:  
  
```  
// C3838a.cpp  
// compile with: /clr /c  
public ref class B : public System::Enum {};   // C3838  
```  
  
 The following sample generates C3838:  
  
```  
// C3838b.cpp  
// compile with: /clr:oldSyntax /c  
public __gc class B : public System::ValueType {};   // C3838  
```