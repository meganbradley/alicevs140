---
title: "operator== (&lt;deque&gt;)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ac48453b-1d26-4776-8eb8-95de2a1d0a00
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator== (&lt;deque&gt;)
Tests if the deque object on the left side of the operator is equal to the deque object on the right side.  
  
## Syntax  
  
```  
  
      bool operator==(  
   const deque<Type, Allocator>& _Left,  
   const deque<Type, Allocator>& _Right  
);  
```  
  
#### Parameters  
 `_Left`  
 An object of type `deque`.  
  
 `_Right`  
 An object of type `deque`.  
  
## Return Value  
 **true** if the deque on the left side of the operator is equal to the deque on the right side of the operator; otherwise **false**.  
  
## Remarks  
 The comparison between deque objects is based on a pairwise comparison of their elements. Two deques are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
## Example  
  
```  
// deque_op_eq.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   deque <int> c1, c2;  
  
   c1.push_back( 1 );  
   c2.push_back( 1 );  
  
   if ( c1 == c2 )  
      cout << "The deques are equal." << endl;  
   else  
      cout << "The deques are not equal." << endl;  
  
   c1.push_back( 1 );  
   if ( c1 == c2 )  
      cout << "The deques are equal." << endl;  
   else  
      cout << "The deques are not equal." << endl;  
}  
```  
  
 **The deques are equal.**  
**The deques are not equal.**   
## Requirements  
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque::operator== and deque::operator<](../vs140/deque--operator==-and-deque--operator-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)