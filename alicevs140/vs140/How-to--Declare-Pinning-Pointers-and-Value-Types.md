---
title: "How to: Declare Pinning Pointers and Value Types"
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
ms.topic: language-reference
ms.assetid: 57c5ec8a-f85a-48c4-ba8b-a81268bcede0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Declare Pinning Pointers and Value Types
A value type can be implicitly boxed. You can then declare a pinning pointer to the value type object itself and use a **pin_ptr** to the boxed value type.  
  
## Example  
  
### Code  
  
```  
// pin_ptr_value.cpp  
// compile with: /clr  
value struct V {  
   int i;  
};  
  
int main() {  
   V ^ v = gcnew V;   // imnplicit boxing  
   v->i=8;  
   System::Console::WriteLine(v->i);  
   pin_ptr<V> mv = &*v;  
   mv->i = 7;  
   System::Console::WriteLine(v->i);  
   System::Console::WriteLine(mv->i);  
}  
```  
  
### Output  
  
```  
8  
7  
7  
```  
  
## See Also  
 [pin_ptr (C++/CLI)](../vs140/pin_ptr--C---CLI-.md)