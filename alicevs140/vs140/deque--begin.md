---
title: "deque::begin"
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
ms.assetid: 0a7d5781-39ce-4df8-9914-4344a0a52b2b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::begin
Returns an iterator addressing the first element in the deque.  
  
## Syntax  
  
```  
  
      const_iterator begin( ) const;   
iterator begin( );  
```  
  
## Return Value  
 A random-access iterator addressing the first element in the deque or to the location succeeding an empty deque.  
  
## Remarks  
 If the return value of **begin** is assigned to a `const_iterator`, the deque object cannot be modified. If the return value of **begin** is assigned to an **iterator**, the deque object can be modified.  
  
## Example  
  
```  
// deque_begin.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   deque <int> c1;  
   deque <int>::iterator c1_Iter;  
   deque <int>::const_iterator c1_cIter;  
  
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
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque Class](../vs140/deque-Class.md)   
 [deque::begin and deque::end](../vs140/deque--begin-and-deque--end.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)