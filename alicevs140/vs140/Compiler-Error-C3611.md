---
title: "Compiler Error C3611"
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
ms.assetid: 42f3e320-41de-420a-bd05-8924cab765aa
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3611
'function': a sealed function cannot have a pure-specifier  
  
 A sealed function was declared incorrectly.  For more information, see [sealed](../vs140/sealed---C---Component-Extensions-.md).  
  
## Example  
 The following sample generates C3611.  
  
```  
// C3611.cpp  
// compile with: /clr /c  
  
ref struct V {  
   virtual void Test() sealed = 0;   // C3611  
   virtual void Test2() sealed;   // OK  
   virtual void Test3() = 0;   // OK  
};  
```