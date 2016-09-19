---
title: "swap Function (auto_handle)"
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
ms.assetid: 7dd91b5c-f0de-4634-a2e2-642626706e27
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap Function (auto_handle)
Swaps objects between one `auto_handle` and another.  
  
## Syntax  
  
```  
template<typename _element_type>  
void swap(  
   auto_handle<_element_type> % _left,  
   auto_handle<_element_type> % _right  
);  
```  
  
#### Parameters  
 `_left`  
 An `auto_handle`.  
  
 `_right`  
 Another `auto_handle`.  
  
## Example  
  
```  
// msl_swap_auto_handle.cpp  
// compile with: /clr  
#include <msclr\auto_handle.h>  
  
using namespace System;  
using namespace msclr;  
  
int main() {  
   auto_handle<String> s1 = "string one";  
   auto_handle<String> s2 = "string two";  
  
   Console::WriteLine( "s1 = '{0}', s2 = '{1}'",  
      s1->ToString(), s2->ToString() );  
   swap( s1, s2 );  
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
 [<msclr\auto_handle.h> Header](../vs140/auto_handle.md)   
 [auto_handle::swap](../vs140/auto_handle--swap.md)