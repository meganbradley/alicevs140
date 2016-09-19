---
title: "deque::max_size"
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
ms.assetid: b1c5ee09-346f-4d4a-bf50-4c97f3f91932
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::max_size
Returns the maximum length of the deque.  
  
## Syntax  
  
```  
  
size_type max_size( ) const;  
  
```  
  
## Return Value  
 The maximum possible length of the deque.  
  
## Example  
  
```  
// deque_max_size.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   deque <int> c1;  
   deque <int>::size_type i;  
  
   i = c1.max_size( );  
   cout << "The maximum possible length of the deque is " << i << "." << endl;  
}  
```  
  
## Sample Output  
  
```  
The maximum possible length of the deque is 1073741823.  
```  
  
## Requirements  
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque Class](../vs140/deque-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)