---
title: "hash_multiset::end"
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
ms.assetid: 8c2d4474-b3fe-4da4-bea0-4adf46798a4c
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multiset::end
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_multiset Class](../vs140/unordered_multiset-Class.md).  
  
 Returns an iterator that addresses the location succeeding the last element in a hash_multiset.  
  
## Syntax  
  
```  
  
      const_iterator end( ) const;   
iterator end( );  
```  
  
## Return Value  
 A bidirectional iterator that addresses the location succeeding the last element in a hash_multiset. If the hash_multiset is empty, then hash_multiset::end == hash_multiset::begin.  
  
## Remarks  
 **end** is used to test whether an iterator has reached the end of its hash_multiset. The value returned by **end** should not be dereferenced.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
  
```  
// hash_multiset_end.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   using namespace stdext;  
   hash_multiset <int> hms1;  
   hash_multiset <int> :: iterator hms1_Iter;  
   hash_multiset <int> :: const_iterator hms1_cIter;  
  
   hms1.insert( 1 );  
   hms1.insert( 2 );  
   hms1.insert( 3 );  
  
   hms1_Iter = hms1.end( );  
   hms1_Iter--;  
   cout << "The last element of hms1 is " << *hms1_Iter << endl;  
  
   hms1.erase( hms1_Iter );  
  
   // The following 3 lines would err because the iterator is const  
   // hms1_cIter = hms1.end( );  
   // hms1_cIter--;  
   // hms1.erase( hms1_cIter );  
  
   hms1_cIter = hms1.end( );  
   hms1_cIter--;  
   cout << "The last element of hms1 is now " << *hms1_cIter << endl;  
}  
```  
  
 **The last element of hms1 is 3**  
**The last element of hms1 is now 2**   
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_multiset Class](../vs140/hash_multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)