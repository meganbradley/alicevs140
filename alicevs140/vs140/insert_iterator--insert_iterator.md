---
title: "insert_iterator::insert_iterator"
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
ms.assetid: a33c8791-09f0-4777-ac72-05773b633da8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# insert_iterator::insert_iterator
Constructs an `insert_iterator` that inserts an element into a specified position in a container.  
  
## Syntax  
  
```  
  
      insert_iterator(  
   Container& _Cont,  
   typename Container::iterator _It  
);  
```  
  
#### Parameters  
 `_Cont`  
 The container into which the `insert_iterator` is to insert elements.  
  
 `_It`  
 The position for the insertion.  
  
## Remarks  
 All containers have the insert member function called by the `insert_iterator`. For associative containers the position parameter is merely a suggestion. The inserter function provides a convenient way to insert to values.  
  
## Example  
  
```  
// insert_iterator_insert_iterator.cpp  
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
   for (i = 1 ; i < 4 ; ++i )    
   {  
      L.push_back ( 10 * i );  
   }  
  
   cout << "The list L is:\n ( ";  
   for ( L_Iter = L.begin( ) ; L_Iter != L.end( ); L_Iter++)  
      cout << *L_Iter << " ";  
   cout << ")." << endl;  
  
   // Using the member function to insert an element  
   inserter ( L, L.begin ( ) ) = 2;  
  
   // Alternatively, you may use the template version  
   insert_iterator< list < int> > Iter(L, L.end ( ) );  
   *Iter = 300;  
  
   cout << "After the insertions, the list L is:\n ( ";  
   for ( L_Iter = L.begin( ) ; L_Iter != L.end( ); L_Iter++ )  
      cout << *L_Iter << " ";  
   cout << ")." << endl;  
}  
```  
  
 **The list L is:**  
 **( 10 20 30 ).**  
**After the insertions, the list L is:**  
 **( 2 10 20 30 300 ).**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [insert_iterator Class](../vs140/insert_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)