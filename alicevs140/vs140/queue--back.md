---
title: "queue::back"
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
ms.assetid: da5af563-e8e3-44ff-8d4a-1ee1535203cd
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queue::back
Returns a reference to the last and most recently added element at the back of the queue.  
  
## Syntax  
  
```  
reference back( );  
const_reference back( ) const;  
```  
  
## Return Value  
 The last element of the queue. If the queue is empty, the return value is undefined.  
  
## Remarks  
 If the return value of **back** is assigned to a `const_reference`, the queue object cannot be modified. If the return value of **back** is assigned to a **reference**, the queue object can be modified.  
  
 When compiling with _SECURE_SCL 1, a runtime error will occur if you attempt to access an element in an empty queue.  See [Checked Iterators](../vs140/Checked-Iterators.md) for more information.  
  
## Example  
  
```  
// queue_back.cpp  
// compile with: /EHsc  
#include <queue>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   queue <int> q1;  
  
   q1.push( 10 );  
   q1.push( 11 );  
  
   int& i = q1.back( );  
   const int& ii = q1.front( );  
  
   cout << "The integer at the back of queue q1 is " << i   
        << "." << endl;  
   cout << "The integer at the front of queue q1 is " << ii   
        << "." << endl;  
}  
```  
  
## Output  
  
```  
The integer at the back of queue q1 is 11.  
The integer at the front of queue q1 is 10.  
```  
  
## Requirements  
 **Header:** <queue\>  
  
 **Namespace:** std  
  
## See Also  
 [queue Class](../vs140/queue-Class.md)   
 [queue Functions](../vs140/queue-Functions.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)