---
title: "vector::size"
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
ms.assetid: df1e9e24-8d4d-4967-9cbe-6bdd108b46cb
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# vector::size
Returns the number of elements in the vector.  
  
## Syntax  
  
```  
  
size_type size( ) const;  
  
```  
  
## Return Value  
 The current length of the vector.  
  
## Example  
  
```  
// vector_size.cpp  
// compile with: /EHsc  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;     
   vector <int> v1;  
   vector <int>::size_type i;  
  
   v1.push_back( 1 );  
   i = v1.size( );  
   cout << "Vector length is " << i << "." << endl;  
  
   v1.push_back( 2 );  
   i = v1.size( );  
   cout << "Vector length is now " << i << "." << endl;  
}  
```  
  
 **Vector length is 1.**  
**Vector length is now 2.**   
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector Class](../vs140/vector-Class.md)   
 [vector::size and vector::capacity](../vs140/vector--size-and-vector--capacity.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)