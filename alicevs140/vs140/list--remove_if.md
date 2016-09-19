---
title: "list::remove_if"
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
ms.assetid: d8ac1b03-7689-4866-8088-cfb9dd5d454d
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# list::remove_if
Erases elements from a list for which a specified predicate is satisfied.  
  
## Syntax  
  
```unstlib  
  
      template<class Predicate>   
void remove_if(  
   Predicate _Pred  
)  
```  
  
#### Parameters  
 `_Pred`  
 The unary predicate which, if satisfied by an element, results in the deletion of that element from the list.  
  
## Example  
  
```  
// list_remove_if.cpp  
// compile with: /EHsc  
#include <list>  
#include <iostream>  
  
template <class T> class is_odd : public std::unary_function<T, bool>   
{  
public:  
   bool operator( ) ( T& val )   
   {  
   return ( val % 2 ) == 1;  
   }  
};  
  
int main( )   
{  
   using namespace std;  
   list <int> c1;  
   list <int>::iterator c1_Iter, c2_Iter;  
  
   c1.push_back( 3 );  
   c1.push_back( 4 );  
   c1.push_back( 5 );  
   c1.push_back( 6 );  
   c1.push_back( 7 );  
   c1.push_back( 8 );  
  
   cout << "The initial list is c1 =";  
   for ( c1_Iter = c1.begin( ); c1_Iter != c1.end( ); c1_Iter++ )  
      cout << " " << *c1_Iter;  
   cout << endl;  
  
   list <int> c2 = c1;  
   c2.remove_if( is_odd<int>( ) );  
  
   cout << "After removing the odd elements, "  
        << "the list becomes c2 =";  
   for ( c2_Iter = c2.begin( ); c2_Iter != c2.end( ); c2_Iter++ )  
      cout << " " << *c2_Iter;  
   cout << endl;  
}  
```  
  
 **The initial list is c1 = 3 4 5 6 7 8**  
**After removing the odd elements, the list becomes c2 = 4 6 8**   
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)