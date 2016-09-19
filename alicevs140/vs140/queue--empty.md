---
title: "queue::empty"
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
ms.assetid: 3625524d-6b82-4389-b8e8-f89010560db8
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queue::empty
Tests if a queue is empty.  
  
## Syntax  
  
```  
  
bool empty( ) const;  
  
```  
  
## Return Value  
 **true** if the queue is empty; **false** if the queue is nonempty.  
  
## Example  
  
```  
// queue_empty.cpp  
// compile with: /EHsc  
#include <queue>  
#include <iostream>  
  
int main( )  
{  
using namespace std;  
  
   // Declares queues with default deque base container  
   queue <int> q1, q2;  
  
   q1.push( 1 );  
  
   if ( q1.empty( ) )  
      cout << "The queue q1 is empty." << endl;  
   else  
      cout << "The queue q1 is not empty." << endl;  
  
   if ( q2.empty( ) )  
      cout << "The queue q2 is empty." << endl;  
   else  
      cout << "The queue q2 is not empty." << endl;  
}  
```  
  
 **The queue q1 is not empty.**  
**The queue q2 is empty.**   
## Requirements  
 **Header:** <queue\>  
  
 **Namespace:** std  
  
## See Also  
 [queue Class](../vs140/queue-Class.md)   
 [queue Functions](../vs140/queue-Functions.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)