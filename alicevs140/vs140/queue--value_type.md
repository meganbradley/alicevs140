---
title: "queue::value_type"
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
ms.assetid: 661f51e1-12e1-495e-8355-dba384919cd9
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queue::value_type
A type that represents the type of object stored as an element in a queue.  
  
## Syntax  
  
```  
typedef typename Container::value_type value_type;  
```  
  
## Remarks  
 The type is a synonym for the `value_type` of the base container adapted by the queue.  
  
## Example  
  
```  
// queue_value_type.cpp  
// compile with: /EHsc  
#include <queue>  
#include <iostream>  
  
int main( )  
{  
using namespace std;  
  
   // Declares queues with default deque base container  
   queue<int>::value_type AnInt;  
  
   AnInt = 69;  
   cout << "The value_type is AnInt = " << AnInt << endl;  
  
   queue<int> q1;  
   q1.push(AnInt);  
   cout << "The element at the front of the queue is "  
        << q1.front( ) << "." << endl;  
}  
```  
  
 **The value_type is AnInt = 69**  
**The element at the front of the queue is 69.**   
## Requirements  
 **Header:** <queue\>  
  
 **Namespace:** std  
  
## See Also  
 [queue Class](../vs140/queue-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)