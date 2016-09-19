---
title: "vector::pointer"
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
ms.assetid: b2e8aaec-c12c-4074-9c05-3dbc33dd8994
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector::pointer
A type that provides a pointer to an element in a vector.  
  
## Syntax  
  
```  
  
typedef typename Allocator::pointer pointer;  
  
```  
  
## Remarks  
 A type **pointer** can be used to modify the value of an element.  
  
## Example  
  
```  
// vector_pointer.cpp  
// compile with: /EHsc  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   vector<int> v;  
   v.push_back( 11 );  
   v.push_back( 22 );  
  
   vector<int>::pointer ptr = &v[0];  
   cout << *ptr << endl;  
   ptr++;  
   cout << *ptr << endl;  
   *ptr = 44;  
   cout << *ptr << endl;  
}  
```  
  
 **11**  
**22**  
**44**   
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector Class](../vs140/vector-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)