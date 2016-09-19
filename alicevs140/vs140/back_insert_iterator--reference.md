---
title: "back_insert_iterator::reference"
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
ms.assetid: 899f61d0-3922-4a22-a338-9400174a8342
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# back_insert_iterator::reference
A type that provides a reference for the `back_insert_iterator`.  
  
## Syntax  
  
```  
  
typedef typename Container::reference reference;  
  
```  
  
## Remarks  
 The type describes a reference to an element of the sequence controlled by the associated container.  
  
## Example  
  
```  
// back_insert_iterator_reference.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   int i;  
  
   vector<int> vec;  
   for (i = 1 ; i < 4 ; ++i )    
   {  
      vec.push_back ( i );  
   }  
  
   vector <int>::iterator vIter;  
   cout << "The vector vec is: ( ";  
   for ( vIter = vec.begin ( ) ; vIter != vec.end ( ); vIter++)  
      cout << *vIter << " ";  
   cout << ")." << endl;  
  
   back_insert_iterator<vector<int> >::reference   
        RefLast = *(vec.end ( ) - 1 );  
   cout << "The last element in the vector vec is: "   
        << RefLast << "." << endl;  
}  
```  
  
 **The vector vec is: ( 1 2 3 ).**  
**The last element in the vector vec is: 3.**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [back_insert_iterator Class](../vs140/back_insert_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)