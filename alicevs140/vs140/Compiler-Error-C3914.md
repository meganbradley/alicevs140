---
title: "Compiler Error C3914"
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
ms.assetid: 8f3190e6-ee50-4916-9ecc-3b8748b2e1e7
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3914
a default property cannot be static  
  
 A default property was declared incorrectly.  For more information, see [How to: Use Indexed Properties](../vs140/How-to--Use-Indexed-Properties.md).  
  
## Example  
 The following sample generates C3914.  
  
```  
// C3914.cpp  
// compile with: /clr /c  
ref struct X {  
   static property int default[int] {   // C3914  
   // try the following line instead  
   // property int default[int] {  
      int get(int) { return 0; }  
      void set(int, int) {}  
   }  
};  
```