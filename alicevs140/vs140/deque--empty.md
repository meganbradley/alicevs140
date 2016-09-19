---
title: "deque::empty"
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
ms.assetid: 79355899-f427-4d6d-9a09-ac5450796378
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::empty
Tests if a deque is empty.  
  
## Syntax  
  
```  
  
bool empty( ) const;  
  
```  
  
## Return Value  
 **true** if the deque is empty; **false** if the deque is not empty.  
  
## Example  
  
```  
// deque_empty.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   deque <int> c1;  
  
   c1.push_back( 10 );  
   if ( c1.empty( ) )  
      cout << "The deque is empty." << endl;  
   else  
      cout << "The deque is not empty." << endl;  
}  
```  
  
 **The deque is not empty.**   
## Requirements  
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque Class](../vs140/deque-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)