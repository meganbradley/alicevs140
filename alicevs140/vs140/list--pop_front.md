---
title: "list::pop_front"
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
ms.assetid: ff984298-33bd-4f37-92cd-34b7717e14c3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::pop_front
Deletes the element at the beginning of a list.  
  
## Syntax  
  
```unstlib  
  
void pop  
_  
front( );  
  
```  
  
## Remarks  
 The first element must not be empty. `pop_front` never throws an exception.  
  
## Example  
  
```  
// list_pop_front.cpp  
// compile with: /EHsc  
#include <list>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   list <int> c1;  
  
   c1.push_back( 1 );  
   c1.push_back( 2 );  
   cout << "The first element is: " << c1.front( ) << endl;  
   cout << "The second element is: " << c1.back( ) << endl;  
  
   c1.pop_front( );  
   cout << "After deleting the element at the beginning of the list, "  
         "the first element is: " << c1.front( ) << endl;  
}  
```  
  
 **The first element is: 1**  
**The second element is: 2**  
**After deleting the element at the beginning of the list, the first element is: 2**   
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)