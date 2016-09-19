---
title: "swap Function (auto_gcroot)"
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
ms.assetid: 2fe8146b-a7f7-445a-9ae9-53b5556be701
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap Function (auto_gcroot)
Swaps objects between one `auto_gcroot` and another.  
  
## Syntax  
  
```  
template<typename _element_type>  
void swap(  
   auto_gcroot<_element_type> & _left,  
   auto_gcroot<_element_type> & _right  
);  
```  
  
#### Parameters  
 `_left`  
 An `auto_gcroot`.  
  
 `_right`  
 Another `auto_gcroot`.  
  
## Example  
  
```  
// msl_swap_auto_gcroot.cpp  
// compile with: /clr  
#include <msclr\auto_gcroot.h>  
  
using namespace System;  
using namespace msclr;  
  
int main() {  
   auto_gcroot<String^> s1 = "string one";  
   auto_gcroot<String^> s2 = "string two";  
  
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
 **Header file** <msclr\auto_gcroot.h>  
  
 **Namespace** msclr  
  
## See Also  
 [<auto_gcroot.h> Header](../vs140/auto_gcroot.md)   
 [auto_gcroot::swap](../vs140/auto_gcroot--swap.md)