---
title: "pop_heap"
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
ms.assetid: 38f6eea3-d192-4597-aae7-c3ec2e659107
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# pop_heap
Removes the largest element from the front of a heap to the next-to-last position in the range and then forms a new heap from the remaining elements.  
  
## Syntax  
  
```  
  
      template<class RandomAccessIterator>  
   void pop_heap(  
      RandomAccessIterator _First,   
      RandomAccessIterator _Last  
   );  
template<class RandomAccessIterator, class BinaryPredicate>  
   void pop_heap(  
      RandomAccessIterator _First,   
      RandomAccessIterator _Last,  
      BinaryPredicate _Comp  
   );  
```  
  
#### Parameters  
 `_First`  
 A random-access iterator addressing the position of the first element in the heap.  
  
 `_Last`  
 A random-access iterator addressing the position one past the final element in the heap.  
  
 `_Comp`  
 User-defined predicate function object that defines sense in which one element is less than another. A binary predicate takes two arguments and returns **true** when satisfied and **false** when not satisfied.  
  
## Remarks  
 The `pop_heap` algorithm is the inverse of the operation performed by the [push_heap](../vs140/push_heap.md) algorithm, in which an element at the next-to-last position of a range is added to a heap consisting of the prior elements in the range, in the case when the element being added to the heap is larger than any of the elements already in the heap.  
  
 Heaps have two properties:  
  
-   The first element is always the largest.  
  
-   Elements may be added or removed in logarithmic time.  
  
 Heaps are an ideal way to implement priority queues and they are used in the implementation of the Standard Template Library container adaptor [priority_queue Class](../vs140/priority_queue-Class.md).  
  
 The range referenced must be valid; all pointers must be dereferenceable and within the sequence the last position is reachable from the first by incrementation.  
  
 The range excluding the newly added element at the end must be a heap.  
  
 The complexity is logarithmic, requiring at most log (*_Last – _First*) comparisons.  
  
## Example  
  
```  
// alg_pop_heap.cpp  
// compile with: /EHsc  
#include <vector>  
#include <algorithm>  
#include <functional>  
#include <iostream>  
  
int main( )  {  
   using namespace std;  
   vector <int> v1;  
   vector <int>::iterator Iter1, Iter2;  
  
   int i;  
   for ( i = 1 ; i <= 9 ; i++ )  
      v1.push_back( i );  
  
   // Make v1 a heap with default less than ordering  
   random_shuffle( v1.begin( ), v1.end( ) );  
   make_heap ( v1.begin( ), v1.end( ) );  
   cout << "The heaped version of vector v1 is ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")." << endl;  
  
   // Add an element to the back of the heap  
   v1.push_back( 10 );  
   push_heap( v1.begin( ), v1.end( ) );  
   cout << "The reheaped v1 with 10 added is ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")." << endl;  
  
   // Remove the largest element from the heap  
   pop_heap( v1.begin( ), v1.end( ) );  
   cout << "The heap v1 with 10 removed is ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")." << endl << endl;  
  
   // Make v1 a heap with greater-than ordering with a 0 element  
   make_heap ( v1.begin( ), v1.end( ), greater<int>( ) );  
   v1.push_back( 0 );  
   push_heap( v1.begin( ), v1.end( ), greater<int>( ) );  
   cout << "The 'greater than' reheaped v1 puts the smallest "  
        << "element first:\n ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")." << endl;  
  
   // Application of pop_heap to remove the smallest element  
   pop_heap( v1.begin( ), v1.end( ), greater<int>( ) );  
   cout << "The 'greater than' heaped v1 with the smallest element\n "  
        << "removed from the heap is: ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")." << endl;  
}  
```  
  
## Sample Output  
  
```  
The heaped version of vector v1 is ( 9 5 8 4 1 6 7 2 3 ).  
The reheaped v1 with 10 added is ( 10 9 8 4 5 6 7 2 3 1 ).  
The heap v1 with 10 removed is ( 9 5 8 4 1 6 7 2 3 10 ).  
  
The 'greater than' reheaped v1 puts the smallest element first:  
 ( 0 1 6 3 2 8 7 4 9 10 5 ).  
The 'greater than' heaped v1 with the smallest element  
 removed from the heap is: ( 1 2 6 3 5 8 7 4 9 10 0 ).  
```  
  
## Requirements  
 **Header:** <algorithm\>  
  
 **Namespace:** std  
  
## See Also  
 [heap](../vs140/heap.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)