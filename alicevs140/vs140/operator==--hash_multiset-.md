---
title: "operator== (hash_multiset)"
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
ms.assetid: b2c47736-0052-466b-8c28-c4ae4edd55be
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator== (hash_multiset)
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Tests if the hash_multiset object on the left side of the operator is equal to the hash_multiset object on the right side.  
  
## Syntax  
  
```  
  
      bool operator!==(  
   const hash_multiset <Key, Traits, Allocator>& _Left,  
   const hash_multiset <Key, Traits, Allocator>& _Right  
);  
```  
  
#### Parameters  
 `_Left`  
 An object of type `hash_multiset`.  
  
 `_Right`  
 An object of type `hash_multiset`.  
  
## Return Value  
 **true** if the hash_multiset on the left side of the operator is equal to the hash_multiset on the right side of the operator; otherwise **false**.  
  
## Remarks  
 The comparison between hash_multiset objects is based on a pairwise comparison of their elements. Two hash_multisets are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
  
```  
// hash_multiset_op_eq.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   using namespace stdext;  
   hash_multiset <int> s1, s2, s3;  
   int i;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      s1.insert ( i );  
      s2.insert ( i * i );  
      s3.insert ( i );  
   }  
  
   if ( s1 == s2 )  
      cout << "The hash_multisets s1 and s2 are equal." << endl;  
   else  
      cout << "The hash_multisets s1 and s2 are not equal." << endl;  
  
   if ( s1 == s3 )  
      cout << "The hash_multisets s1 and s2 are equal." << endl;  
   else  
      cout << "The hash_multisets s1 and s2 are not equal." << endl;  
}  
```  
  
 **The hash_multisets s1 and s2 are not equal.**  
**The hash_multisets s1 and s2 are equal.**   
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)