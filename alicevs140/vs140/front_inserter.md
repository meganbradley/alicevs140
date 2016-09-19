---
title: "front_inserter"
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
ms.assetid: 236f3f00-77aa-47ba-9eff-c1c91e784172
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# front_inserter
Creates an iterator that can insert elements at the front of a specified container.  
  
## Syntax  
  
```  
  
   template<class Container>  
front_insert_iterator<Container> front_inserter(  
   Container& _Cont  
);  
```  
  
#### Parameters  
 `_Cont`  
 The container object whose front is having an element inserted.  
  
## Return Value  
 A `front_insert_iterator` associated with the container object `_Cont`.  
  
## Remarks  
 The member function [front_insert_iterator](../vs140/front_insert_iterator--front_insert_iterator.md) of the front_insert_iterator class may also be used.  
  
 Within the Standard Template Library, the argument must refer to one of the two sequence containers that have the member function `push_back`: [deque Class](../vs140/deque-Class.md) or [list Class](../vs140/list-Class.md).  
  
## Example  
  
```  
// iterator_front_inserter.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <list>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   int i;  
   list <int>::iterator L_Iter;  
  
   list<int> L;  
   for ( i = -1 ; i < 9 ; ++i )  
   {  
      L.push_back ( i );  
   }  
  
   cout << "The list L is:\n ( ";  
   for ( L_Iter = L.begin( ) ; L_Iter != L.end( ); L_Iter++)  
      cout << *L_Iter << " ";  
   cout << ")." << endl;  
  
   // Using the template function to insert an element  
   front_insert_iterator< list < int> > Iter(L);  
   *Iter = 100;  
  
   // Alternatively, you may use the front_insert member function  
   front_inserter ( L ) = 200;  
  
   cout << "After the front insertions, the list L is:\n ( ";  
   for ( L_Iter = L.begin( ) ; L_Iter != L.end( ); L_Iter++)  
      cout << *L_Iter << " ";  
   cout << ")." << endl;  
}  
```  
  
 **The list L is:**  
 **( -1 0 1 2 3 4 5 6 7 8 ).**  
**After the front insertions, the list L is:**  
 **( 200 100 -1 0 1 2 3 4 5 6 7 8 ).**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)