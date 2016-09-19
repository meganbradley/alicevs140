---
title: "multiset::crbegin"
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
ms.assetid: 87596713-91ef-4254-9f78-9cc037db8f49
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::crbegin
Returns a const iterator addressing the first element in a reversed multiset.  
  
## Syntax  
  
```  
  
const_reverse_iterator crbegin( ) const;  
  
```  
  
## Return Value  
 A const reverse bidirectional iterator addressing the first element in a reversed multiset or addressing what had been the last element in the unreversed multiset.  
  
## Remarks  
 `crbegin` is used with a reversed multiset just as [begin](#vclrfmultisetrbegin) is used with a multiset.  
  
 With the return value of `crbegin`, the multiset object cannot be modified.  
  
 `crbegin` can be used to iterate through a multiset backwards.  
  
## Example  
  
```  
// multiset_crbegin.cpp  
// compile with: /EHsc  
#include <set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;     
   multiset <int> ms1;  
   multiset <int>::const_reverse_iterator ms1_crIter;  
  
   ms1.insert( 10 );  
   ms1.insert( 20 );  
   ms1.insert( 30 );  
  
   ms1_crIter = ms1.crbegin( );  
   cout << "The first element in the reversed multiset is "  
        << *ms1_crIter << "." << endl;  
}  
```  
  
 **The first element in the reversed multiset is 30.**   
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [multiset Class](../vs140/multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)