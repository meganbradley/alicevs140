---
title: "set::size"
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
ms.assetid: b5b808f7-dba2-4da8-8c8b-48df2d7f1677
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# set::size
Returns the number of elements in the set.  
  
## Syntax  
  
```  
  
size_type size( ) const;  
  
```  
  
## Return Value  
 The current length of the set.  
  
## Example  
  
```  
// set_size.cpp  
// compile with: /EHsc  
#include <set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   set <int> s1;  
   set <int> :: size_type i;  
  
   s1.insert( 1 );  
   i = s1.size( );  
   cout << "The set length is " << i << "." << endl;  
  
   s1.insert( 2 );  
   i = s1.size( );  
   cout << "The set length is now " << i << "." << endl;  
}  
```  
  
 **The set length is 1.**  
**The set length is now 2.**   
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [set::size](../vs140/set--size--STL-Samples-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)