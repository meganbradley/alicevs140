---
title: "operator!= (multimap)"
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
ms.assetid: 8b50c4ab-ffdf-48de-8ece-f3c96549667b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator!= (multimap)
Tests if the multimap object on the left side of the operator is not equal to the multimap object on the right side.  
  
## Syntax  
  
```  
  
      bool operator!=(  
   const multimap <Key, Type, Traits, Allocator>& _Left,  
   const multimap <Key, Type, Traits, Allocator>& _Right  
);  
```  
  
#### Parameters  
 `_Left`  
 An object of type `multimap`.  
  
 `_Right`  
 An object of type `multimap`.  
  
## Return Value  
 **true** if the multimaps are not equal; **false** if multimaps are equal.  
  
## Remarks  
 The comparison between multimap objects is based on a pairwise comparison of their elements. Two multimaps are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
## Example  
  
```  
// multimap_op_ne.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   multimap <int, int> m1, m2, m3;  
   int i;  
   typedef pair <int, int> Int_Pair;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i ) );  
   }  
  
   if ( m1 != m2 )  
      cout << "The multimaps m1 and m2 are not equal." << endl;  
   else  
      cout << "The multimaps m1 and m2 are equal." << endl;  
  
   if ( m1 != m3 )  
      cout << "The multimaps m1 and m3 are not equal." << endl;  
   else  
      cout << "The multimaps m1 and m3 are equal." << endl;  
}  
```  
  
 **The multimaps m1 and m2 are not equal.**  
**The multimaps m1 and m3 are equal.**   
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)