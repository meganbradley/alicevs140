---
title: "novtable"
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
ms.assetid: cfef09c5-8c1e-4b14-8a72-7d726ded4484
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# novtable
## Microsoft Specific  
 This is a `__declspec` extended attribute.  
  
 This form of `__declspec` can be applied to any class declaration, but should only be applied to pure interface classes, that is, classes that will never be instantiated on their own. The `__declspec` stops the compiler from generating code to initialize the vfptr in the constructor(s) and destructor of the class. In many cases, this removes the only references to the vtable that are associated with the class and, thus, the linker will remove it. Using this form of `__declspec` can result in a significant reduction in code size.  
  
 If you attempt to instantiate a class marked with `novtable` and then access a class member, you will receive an access violation (AV).  
  
## Example  
  
```  
// novtable.cpp  
#include <stdio.h>  
  
struct __declspec(novtable) X {  
   virtual void mf();  
};  
  
struct Y : public X {  
   void mf() {  
      printf_s("In Y\n");  
   }  
};  
  
int main() {  
   // X *pX = new X();  
   // pX->mf();   // Causes a runtime access violation.  
  
   Y *pY = new Y();  
   pY->mf();  
}  
```  
  
 **In Y**   
## END Microsoft Specific  
  
## See Also  
 [__declspec](../vs140/__declspec.md)   
 [Keywords](../vs140/Keywords--C---.md)