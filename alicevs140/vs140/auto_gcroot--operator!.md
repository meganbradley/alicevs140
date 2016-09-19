---
title: "auto_gcroot::operator!"
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
ms.topic: reference
ms.assetid: f9728be3-2e09-4c01-a594-43e0d59d40d3
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_gcroot::operator!
Operator for using `auto_gcroot` in a conditional expression.  
  
## Syntax  
  
```  
bool operator!() const;  
```  
  
## Return Value  
 `true` if the wrapped object is invalid; `false` otherwise.  
  
## Example  
  
```  
// msl_auto_gcroot_operator_not.cpp  
// compile with: /clr  
#include <msclr\auto_gcroot.h>  
  
using namespace System;  
using namespace msclr;  
  
int main() {  
   auto_gcroot<String^> s;  
   if ( s ) Console::WriteLine( "s is valid" );  
   if ( !s ) Console::WriteLine( "s is invalid" );  
   s = "something";  
   if ( s ) Console::WriteLine( "now s is valid" );  
   if ( !s ) Console::WriteLine( "now s is invalid" );  
   s.reset();  
   if ( s ) Console::WriteLine( "now s is valid" );  
   if ( !s ) Console::WriteLine( "now s is invalid" );  
}  
```  
  
 **s is invalid**  
**now s is valid**  
**now s is invalid**   
## Requirements  
 **Header file** <msclr\auto_gcroot.h>  
  
 **Namespace** msclr  
  
## See Also  
 [auto_gcroot Members](../vs140/auto_gcroot-Members.md)   
 [auto_gcroot::operator bool](../vs140/auto_gcroot--operator-bool.md)