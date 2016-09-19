---
title: "Compiler Error C3159"
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
ms.assetid: e115cc76-0021-4568-95fd-61a324c41a85
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3159
'pointer' : array of pointers to value type cannot be declared  
  
 An array of pointers to a value type cannot be declared.  
  
 C3159 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3159:  
  
```  
// C3159.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
  
__value struct B {  
};  
  
void f( B*[] );   // C3159  
  
int main() {  
}  
```