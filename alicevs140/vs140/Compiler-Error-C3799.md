---
title: "Compiler Error C3799"
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
ms.assetid: 336a2811-9370-4e6e-b03b-325bda470805
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3799
indexed property cannot have an empty parameter list  
  
 An indexed property was declared incorrectly.  See [How to: Use Indexed Properties](../vs140/How-to--Use-Indexed-Properties.md) for more information.  
  
## Example  
 The following sample generates C3799.  
  
```  
// C3799.cpp  
// compile with: /clr /c  
ref struct C {  
   property int default[] {   // C3799  
   // try the following line instead  
   // property int default[int] {  
      int get(int index) { return 0; }  
      void set(int index, int value) {}  
   }  
};  
```