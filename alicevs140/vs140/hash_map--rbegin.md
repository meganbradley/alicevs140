---
title: "hash_map::rbegin"
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
ms.assetid: 5f24cf2d-500f-4a09-bacc-34eb0133fbee
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::rbegin
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_map Class](../vs140/unordered_map-Class.md).  
  
 Returns an iterator addressing the first element in a reversed hash_map.  
  
## Syntax  
  
```  
  
      const_reverse_iterator rbegin( ) const;   
reverse_iterator rbegin( );  
```  
  
## Return Value  
 A reverse bidirectional iterator addressing the first element in a reversed hash_map or addressing what had been the last element in the unreversed hash_map.  
  
## Remarks  
 `rbegin` is used with a reversed hash_map just as [begin](../vs140/hash_map--begin.md) is used with a hash_map.  
  
 If the return value of `rbegin` is assigned to a [const_reverse_iterator](../vs140/hash_map--const_reverse_iterator.md), then the hash_map object cannot be modified. If the return value of `rbegin` is assigned to a [reverse_iterator](../vs140/hash_map--reverse_iterator.md), then the hash_map object can be modified.  
  
 `rbegin` can be used to iterate through a hash_map backwards.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
  
```  
// hash_map_rbegin.cpp  
// compile with: /EHsc  
#include <hash_map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   using namespace stdext;  
   hash_map <int, int> hm1;  
  
   hash_map <int, int> :: iterator hm1_Iter;  
   hash_map <int, int> :: reverse_iterator hm1_rIter;  
   hash_map <int, int> :: const_reverse_iterator hm1_crIter;  
   typedef pair <int, int> Int_Pair;  
  
   hm1.insert ( Int_Pair ( 1, 10 ) );  
   hm1.insert ( Int_Pair ( 2, 20 ) );  
   hm1.insert ( Int_Pair ( 3, 30 ) );  
  
   hm1_rIter = hm1.rbegin( );  
   cout << "The first element of the reversed hash_map hm1 is "  
        << hm1_rIter -> first << "." << endl;  
  
   // begin can be used to start an iteration   
   // through a hash_map in a forward order  
   cout << "The hash_map is: ";  
   for ( hm1_Iter = hm1.begin( ) ; hm1_Iter != hm1.end( ); hm1_Iter++)  
      cout << hm1_Iter -> first << " ";  
      cout << "." << endl;  
  
   // rbegin can be used to start an iteration   
   // through a hash_map in a reverse order  
   cout << "The reversed hash_map is: ";  
   for ( hm1_rIter = hm1.rbegin( ) ; hm1_rIter != hm1.rend( ); hm1_rIter++)  
      cout << hm1_rIter -> first << " ";  
      cout << "." << endl;  
  
   // A hash_map element can be erased by dereferencing to its key   
   hm1_rIter = hm1.rbegin( );  
   hm1.erase ( hm1_rIter -> first );  
  
   hm1_rIter = hm1.rbegin( );  
   cout << "After the erasure, the first element "  
        << "in the reversed hash_map is "  
        << hm1_rIter -> first << "." << endl;  
}  
```  
  
 **The first element of the reversed hash_map hm1 is 3.**  
**The hash_map is: 1 2 3 .**  
**The reversed hash_map is: 3 2 1 .**  
**After the erasure, the first element in the reversed hash_map is 2.**   
## Requirements  
 **Header:** <hash_map>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_map Class](../vs140/hash_map-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)