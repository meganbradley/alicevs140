---
title: "vector::empty"
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
ms.assetid: e9d8ef6d-3ee2-4959-a4f1-cd1c5583cde4
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector::empty
Tests if the vector is empty.  
  
## Syntax  
  
```  
  
bool empty( ) const;  
  
```  
  
## Return Value  
 **true** if the vector is empty; **false** if the vector is not empty.  
  
## Example  
  
```  
// vector_empty.cpp  
// compile with: /EHsc  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;     
   vector <int> v1;  
  
   v1.push_back( 10 );  
  
   if ( v1.empty( ) )  
      cout << "The vector is empty." << endl;  
   else  
      cout << "The vector is not empty." << endl;  
}  
```  
  
 **The vector is not empty.**   
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector Class](../vs140/vector-Class.md)   
 [vector::empty, vector::erase, and vector::push_back](../vs140/vector--empty--vector--erase--and-vector--push_back.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)