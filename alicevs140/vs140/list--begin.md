---
title: "list::begin"
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
ms.assetid: ef8c4030-3746-4c81-a6ee-e3ed4b4c8204
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::begin
Returns an iterator addressing the first element in a list.  
  
## Syntax  
  
```  
  
      const  
      _  
      iterator begin( ) const;  
iterator begin( );  
```  
  
## Return Value  
 A bidirectional iterator addressing the first element in the list or to the location succeeding an empty list.  
  
## Remarks  
 If the return value of **begin** is assigned to a `const_iterator`, the elements in the list object cannot be modified. If the return value of **begin** is assigned to an **iterator**, the elements in the list object can be modified.  
  
## Example  
  
```  
// list_begin.cpp  
// compile with: /EHsc  
#include <list>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   list <int> c1;  
   list <int>::iterator c1_Iter;  
   list <int>::const_iterator c1_cIter;  
  
   c1.push_back( 1 );  
   c1.push_back( 2 );  
  
   c1_Iter = c1.begin( );  
   cout << "The first element of c1 is " << *c1_Iter << endl;  
  
   *c1_Iter = 20;  
   c1_Iter = c1.begin( );  
   cout << "The first element of c1 is now " << *c1_Iter << endl;  
  
   // The following line would be an error because iterator is const  
   // *c1_cIter = 200;  
}  
```  
  
 **The first element of c1 is 1**  
**The first element of c1 is now 20**   
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)