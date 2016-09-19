---
title: "operator== (&lt;stack&gt;)"
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
ms.assetid: a3c64548-badb-40ae-a3ee-c523adcfe956
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator== (&lt;stack&gt;)
Tests if the stack object on the left side of the operator is equal to stack object on the right side.  
  
## Syntax  
  
```  
  
      bool operator==(  
   const stack <Type, Container>& _Left,  
   const stack <Type, Container>& _Right  
);  
```  
  
#### Parameters  
 `_Left`  
 An object of type **stack**.  
  
 `_Right`  
 An object of type **stack**.  
  
## Return Value  
 **true** if the stacks or stacks are equal; **false** if stacks or stacks are not equal.  
  
## Remarks  
 The comparison between stack objects is based on a pairwise comparison of their elements. Two stacks are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
## Example  
  
```  
// stack_op_eq.cpp  
// compile with: /EHsc  
#include <stack>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   // Declares stacks with vector base containers  
   stack <int, vector<int> > s1, s2, s3;  
  
   // The following would have cause an error because stacks with  
   // different base containers are not equality comparable  
   // stack <int, list<int> > s3;  
  
   s1.push( 1 );  
   s2.push( 2 );  
   s3.push( 1 );  
  
   if ( s1 == s2 )  
      cout << "The stacks s1 and s2 are equal." << endl;  
   else  
      cout << "The stacks s1 and s2 are not equal." << endl;  
  
   if ( s1 == s3 )  
      cout << "The stacks s1 and s3 are equal." << endl;  
   else  
      cout << "The stacks s1 and s3 are not equal." << endl;  
}  
```  
  
 **The stacks s1 and s2 are not equal.**  
**The stacks s1 and s3 are equal.**   
## Requirements  
 **Header:** <stack\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)