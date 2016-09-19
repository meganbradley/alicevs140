---
title: "list::size"
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
ms.assetid: a8021f82-ff4f-48de-83ab-13b470dd65ac
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::size
Returns the number of elements in a list.  
  
## Syntax  
  
```unstlib  
  
size  
_  
type size( ) const;  
  
```  
  
## Return Value  
 The current length of the list.  
  
## Example  
  
```  
// list_size.cpp  
// compile with: /EHsc  
#include <list>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   list <int> c1;  
   list <int>::size_type i;  
  
   c1.push_back( 5 );  
   i = c1.size( );  
   cout << "List length is " << i << "." << endl;  
  
   c1.push_back( 7 );  
   i = c1.size( );  
   cout << "List length is now " << i << "." << endl;  
}  
```  
  
 **List length is 1.**  
**List length is now 2.**   
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)