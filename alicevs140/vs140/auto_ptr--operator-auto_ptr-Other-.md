---
title: "auto_ptr::operator auto_ptr&lt;Other&gt;"
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
ms.topic: article
ms.assetid: d77dd9b0-3115-47ce-ab27-10bae32a803b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_ptr::operator auto_ptr&lt;Other&gt;
Casts from one kind of `auto_ptr` to another kind of `auto_ptr`.  
  
## Syntax  
  
```  
  
   template<class Other>  
operator auto_ptr<Other>( ) throw( );  
```  
  
## Return Value  
 The type cast operator returns `auto_ptr` <**Other**>(**\*this**).  
  
## Example  
  
```  
// auto_ptr_op_auto_ptr.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
int main()  
{  
   auto_ptr<int> pi ( new int( 5 ) );  
   auto_ptr<const int> pc = ( auto_ptr<const int> )pi;  
}  
```  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [auto_ptr Class](../vs140/auto_ptr-Class.md)