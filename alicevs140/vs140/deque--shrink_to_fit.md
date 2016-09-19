---
title: "deque::shrink_to_fit"
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
ms.assetid: 3df4a2c1-eb32-42a9-9dc9-207bbc2ad8b6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::shrink_to_fit
Discards excess capacity.  
  
## Syntax  
  
```  
void shrink_to_fit(  
);  
```  
  
## Remarks  
 There is no portable way to determine if `shrink_to_fit` reduces the storage used by a [deque](../vs140/deque-Class.md).  
  
## Example  
  
```  
// deque_shrink_to_fit.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;     
   deque <int> v1;  
   //deque <int>::iterator Iter;  
  
   v1.push_back( 1 );  
   v1.push_back( 2 );  
   cout << "Current size of v1 = "   
      << v1.size( ) << endl;  
   v1.shrink_to_fit();  
   cout << "Current size of v1 = "   
      << v1.size( ) << endl;  
}  
```  
  
 **Current size of v1 = 1**  
**Current size of v1 = 1**   
## Requirements  
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque Class](../vs140/deque-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)