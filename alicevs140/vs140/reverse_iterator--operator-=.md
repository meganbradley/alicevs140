---
title: "reverse_iterator::operator+="
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
ms.assetid: 1a24f7f2-1bdb-4599-aa0b-fd8dc1e17d32
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# reverse_iterator::operator+=
Adds a specified offset from a reverse_iterator.  
  
## Syntax  
  
```  
reverse_iterator<RandomIterator>& operator+=(  
   difference_type _Off  
);  
```  
  
#### Parameters  
 `_Off`  
 The offset by which to increment the iterator.  
  
## Return Value  
 A reference to the element addressed by the `reverse_iterator`.  
  
## Example  
  
```  
// reverse_iterator_op_addoff.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   int i;  
  
   vector<int> vec;  
   for (i = 1 ; i < 6 ; ++i )   
   {  
      vec.push_back ( 2 * i );  
   }  
  
   vector <int>::iterator vIter;  
  
   cout << "The vector vec is: ( ";  
   for ( vIter = vec.begin( ) ; vIter != vec.end( ); vIter++)  
      cout << *vIter << " ";  
   cout << ")." << endl;  
  
   vector <int>::reverse_iterator rvIter;  
   cout << "The vector vec reversed is: ( ";  
   for ( rvIter = vec.rbegin( ) ; rvIter != vec.rend( ); rvIter++)  
      cout << *rvIter << " ";  
   cout << ")." << endl;  
  
   // Initializing reverse_iterators to the last element  
   vector <int>::reverse_iterator rVPOS1 = vec.rbegin ( );  
  
   cout << "The iterator rVPOS1 initially points to the first "  
        << "element\n in the reversed sequence: "  
        << *rVPOS1 << "." << endl;  
  
   rVPOS1+=2;   // addition of an offset  
   cout << "After the +2 offset, the iterator rVPOS1 now points\n"  
        << " to the third element in the reversed sequence: "  
        << *rVPOS1 << "." << endl;  
}  
```  
  
 **The vector vec is: ( 2 4 6 8 10 ).**  
**The vector vec reversed is: ( 10 8 6 4 2 ).**  
**The iterator rVPOS1 initially points to the first element**  
 **in the reversed sequence: 10.**  
**After the +2 offset, the iterator rVPOS1 now points**  
 **to the third element in the reversed sequence: 6.**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [reverse_iterator Class](../vs140/reverse_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)