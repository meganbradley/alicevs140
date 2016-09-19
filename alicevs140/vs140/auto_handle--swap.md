---
title: "auto_handle::swap"
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
ms.assetid: 3ebf82d7-9b69-4a72-a22d-69b4f640f9b0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_handle::swap
Swaps objects with another `auto_handle`.  
  
## Syntax  
  
```  
void swap(  
   auto_handle<_element_type> % _right  
);  
```  
  
#### Parameters  
 `_right`  
 The `auto_handle` with which to swap objects.  
  
## Example  
  
```  
// msl_auto_handle_swap.cpp  
// compile with: /clr  
#include <msclr\auto_handle.h>  
  
using namespace System;  
using namespace msclr;  
  
int main() {  
   auto_handle<String> s1 = "string one";  
   auto_handle<String> s2 = "string two";  
  
   Console::WriteLine( "s1 = '{0}', s2 = '{1}'",  
      s1->ToString(), s2->ToString() );  
   s1.swap( s2 );  
   Console::WriteLine( "s1 = '{0}', s2 = '{1}'",  
      s1->ToString(), s2->ToString() );  
}  
```  
  
 **s1 = 'string one', s2 = 'string two'**  
**s1 = 'string two', s2 = 'string one'**   
## Requirements  
 **Header file** <msclr\auto_handle.h>  
  
 **Namespace** msclr  
  
## See Also  
 [auto_handle Members](../vs140/auto_handle-Members.md)   
 [swap Function (<msclr\auto_handle.h>)](../vs140/swap-Function--auto_handle-.md)