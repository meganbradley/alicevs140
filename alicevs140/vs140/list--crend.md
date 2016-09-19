---
title: "list::crend"
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
ms.assetid: 60922007-b4df-4716-b309-4f4ea40fb570
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::crend
Returns a const iterator that addresses the location succeeding the last element in a reversed list.  
  
## Syntax  
  
```  
  
const  
_  
reverse  
_  
iterator rend( ) const;  
  
```  
  
## Return Value  
 A const reverse bidirectional iterator that addresses the location succeeding the last element in a reversed [list](../vs140/list-Class.md) (the location that had preceded the first element in the unreversed `list`).  
  
## Remarks  
 `crend` is used with a reversed list just as [end](../vs140/list--end.md) is used with a `list`.  
  
 With the return value of `crend`, the `list` object cannot be modified.  
  
 `crend` can be used to test to whether a reverse iterator has reached the end of its `list`.  
  
 The value returned by `crend` should not be dereferenced.  
  
## Example  
  
```  
// list_crend.cpp  
// compile with: /EHsc  
#include <list>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   list <int> c1;  
   list <int>::const_reverse_iterator c1_crIter;  
  
   c1.push_back( 10 );  
   c1.push_back( 20 );  
   c1.push_back( 30 );  
  
   c1_crIter = c1.crend( );  
   c1_crIter --;  // Decrementing a reverse iterator moves it forward in   
                 // the list (to point to the first element here)  
   cout << "The first element in the list is: " << *c1_crIter << endl;  
}  
```  
  
 **The first element in the list is: 10**   
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)