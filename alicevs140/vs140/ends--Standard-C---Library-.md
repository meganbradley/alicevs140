---
title: "ends (Standard C++ Library)"
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
ms.assetid: 98f6faf9-813f-474e-8ef7-3e0d613f2024
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# ends (Standard C++ Library)
Terminates a string.  
  
## Syntax  
  
```  
  
      template class<  
      _Elem  
      ,   
      _Tr>  
   basic_ostream<_Elem, _Tr>& ends(  
      basic_ostream<_Elem, _Tr>& _Ostr  
);  
```  
  
#### Parameters  
 `_Elem`  
 The element type.  
  
 `_Ostr`  
 An object of type `basic_ostream`.  
  
 `_Tr`  
 Character traits.  
  
## Return Value  
 An object of type `basic_ostream`.  
  
## Remarks  
 The manipulator calls `_Ostr`**.**[put](../vs140/basic_ostream--put.md)(`_Elem`(**'\0'**)). It returns `_Ostr.`  
  
## Example  
  
```  
// ostream_ends.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   cout << "a";  
   cout << "b" << ends;  
   cout << "c" << endl;  
}  
```  
  
 **ab c**   
## Requirements  
 **Header:** <ostream\>  
  
 **Namespace:** std  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)