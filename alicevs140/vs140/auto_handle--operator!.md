---
title: "auto_handle::operator!"
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
ms.assetid: 3f6c7729-3260-4842-87f9-c491c140b299
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_handle::operator!
Operator for using `auto_handle` in a conditional expression.  
  
## Syntax  
  
```  
bool operator!();  
```  
  
## Return Value  
 `true` if the wrapped object is invalid; `false` otherwise.  
  
## Example  
  
```  
// msl_auto_handle_operator_not.cpp  
// compile with: /clr  
#include <msclr\auto_handle.h>  
  
using namespace System;  
using namespace msclr;  
  
int main() {  
   auto_handle<String> s1;  
   auto_handle<String> s2 = "something";  
   if ( s1) Console::WriteLine( "s1 is valid" );  
   if ( !s1 ) Console::WriteLine( "s1 is invalid" );  
   if ( s2 ) Console::WriteLine( "s2 is valid" );  
   if ( !s2 ) Console::WriteLine( "s2 is invalid" );  
   s2.reset();  
   if ( s2 ) Console::WriteLine( "s2 is now valid" );  
   if ( !s2 ) Console::WriteLine( "s2 is now invalid" );  
}  
```  
  
 **s1 is invalid**  
**s2 is valid**  
**s2 is now invalid**   
## Requirements  
 **Header file** <msclr\auto_handle.h>  
  
 **Namespace** msclr  
  
## See Also  
 [auto_handle Members](../vs140/auto_handle-Members.md)   
 [auto_handle::operator bool](../vs140/auto_handle--operator-bool.md)