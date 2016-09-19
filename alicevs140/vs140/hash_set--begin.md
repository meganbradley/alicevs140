---
title: "hash_set::begin"
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
ms.assetid: e4828414-8719-4f0a-a253-5570ab7a5f66
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_set::begin
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Returns an iterator that addresses the first element in the hash_set.  
  
## Syntax  
  
```  
  
      const_iterator begin( ) const;   
iterator begin( );  
```  
  
## Return Value  
 A bidirectional iterator addressing the first element in the hash_set or the location succeeding an empty hash_set.  
  
## Remarks  
 If the return value of **begin** is assigned to a `const_iterator`, the elements in the hash_set object cannot be modified. If the return value of **begin** is assigned to an **iterator**, the elements in the hash_set object can be modified.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
  
```  
// hash_set_begin.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   using namespace stdext;  
   hash_set <int> hs1;  
   hash_set <int>::iterator hs1_Iter;  
   hash_set <int>::const_iterator hs1_cIter;  
  
   hs1.insert( 1 );  
   hs1.insert( 2 );  
   hs1.insert( 3 );  
  
   hs1_Iter = hs1.begin( );  
   cout << "The first element of hs1 is " << *hs1_Iter << endl;  
  
   hs1_Iter = hs1.begin( );  
   hs1.erase( hs1_Iter );  
  
   // The following 2 lines would err because the iterator is const  
   // hs1_cIter = hs1.begin( );  
   // hs1.erase( hs1_cIter );  
  
   hs1_cIter = hs1.begin( );  
   cout << "The first element of hs1 is now " << *hs1_cIter << endl;  
}  
```  
  
 **The first element of hs1 is 1**  
**The first element of hs1 is now 2**   
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_set Class](../vs140/hash_set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)