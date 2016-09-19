---
title: "Compiler Error C3155"
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
ms.assetid: b04a42e1-64e7-40f8-81fe-c7945348b2cf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3155
attributes are not allowed in a property indexer  
  
 An indexed property was declared incorrectly. For more information, see [How to: Use Indexed Properties](../vs140/How-to--Use-Indexed-Properties.md).  
  
## Example  
 The following sample generates C3155.  
  
```  
// C3155.cpp  
// compile with: /clr /c  
using namespace System;  
ref struct R {  
   property int F[[ParamArray] int] {   // C3155  
   // try the following line instead  
   // property int F[ int] {   // OK  
      int get(int i) {   
         return 0;   
      }  
   }  
};  
```