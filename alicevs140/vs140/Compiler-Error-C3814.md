---
title: "Compiler Error C3814"
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
ms.assetid: bac2a329-5cdd-4092-bf75-233ecbad056b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3814
'class member' : this member cannot co-exist with a property of the same name  
  
 A property and another class member have the same identifier. To fix this error, change one of the identifiers.  
  
 C3814 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3814:  
  
```  
// C3814.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
__gc class CMyClass {  
public:  
   char Size;  
   __property int get_Size() {return __Size;}   // C3814  
   __property void set_Size(int value) {__Size=value;}   // C3814  
protected:  
   int __Size;  
};  
  
int main() {  
}  
```