---
title: "&lt;hash_set&gt; operators"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 403d8e4e-0b3f-43fb-bc5a-8100c4f331c5
caps.latest.revision: 11
---
# &lt;hash_set&gt; operators
||||  
|-|-|-|  
|[operator!=](#operator_neq)|[operator!= (hash_multiset)](#operator_neq__hash_multiset_)|[operator==](#operator_eq_eq)|  
|[operator== (hash_multiset)](#operator_eq_eq__hash_multiset_)|  
  
##  <a name="operator_neq"></a>  operator!=  
  
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Tests if the hash_set object on the left side of the operator is not equal to the hash_set object on the right side.  
  
```  
bool operator!=(    const hash_set <Key, Traits, Allocator>&  _Left ,    const hash_set <Key, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `hash_set`.  
  
 `_Right`  
 An object of type `hash_set`.  
  
### Return Value  
 **true** if the hash_sets are not equal; **false** if hash_sets are equal.  
  
### Remarks  
 The comparison between hash_set objects is based on a pairwise comparison between their elements. Two hash_sets are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
### Example  
  
```  
// hash_set_op_ne.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   using namespace stdext;  
   hash_set <int> hs1, hs2, hs3;  
   int i;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      hs1.insert ( i );  
      hs2.insert ( i * i );  
      hs3.insert ( i );  
   }  
  
   if ( hs1 != hs2 )  
      cout << "The hash_sets hs1 and hs2 are not equal." << endl;  
   else  
      cout << "The hash_sets hs1 and hs2 are equal." << endl;  
  
   if ( hs1 != hs3 )  
      cout << "The hash_sets hs1 and hs3 are not equal." << endl;  
   else  
      cout << "The hash_sets hs1 and hs3 are equal." << endl;  
}  
```  
  
  **The hash_sets hs1 and hs2 are not equal.**  
**The hash_sets hs1 and hs3 are equal.**    
##  <a name="operator_eq_eq"></a>  operator==  
  
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Tests if the hash_set object on the left side of the operator is equal to the hash_set object on the right side.  
  
```  
bool operator!==(    const hash_set <Key, Traits, Allocator>&  _Left ,    const hash_set <Key, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `hash_set`.  
  
 `_Right`  
 An object of type `hash_set`.  
  
### Return Value  
 **true** if the hash_set on the left side of the operator is equal to the hash_set on the right side of the operator; otherwise **false**.  
  
### Remarks  
 The comparison between hash_set objects is based on a pairwise comparison of their elements. Two hash_sets are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
### Example  
  
```  
// hash_set_op_eq.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   using namespace stdext;  
   hash_set <int> s1, s2, s3;  
   int i;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      s1.insert ( i );  
      s2.insert ( i * i );  
      s3.insert ( i );  
   }  
  
   if ( s1 == s2 )  
      cout << "The hash_sets s1 and s2 are equal." << endl;  
   else  
      cout << "The hash_sets s1 and s2 are not equal." << endl;  
  
   if ( s1 == s3 )  
      cout << "The hash_sets s1 and s3 are equal." << endl;  
   else  
      cout << "The hash_sets s1 and s3 are not equal." << endl;  
}  
```  
  
  **The hash_sets s1 and s2 are not equal.**  
**The hash_sets s1 and s3 are equal.**    
##  <a name="operator_neq__hash_multiset_"></a>  operator!= (hash_multiset)  
  
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Tests if the hash_multiset object on the left side of the operator is not equal to the hash_multiset object on the right side.  
  
```  
bool operator!=(    const hash_multiset <Key, Traits, Allocator>&  _Left ,    const hash_multiset <Key, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `hash_multiset`.  
  
 `_Right`  
 An object of type `hash_multiset`.  
  
### Return Value  
 **true** if the hash_multisets are not equal; **false** if hash_multisets are equal.  
  
### Remarks  
 The comparison between hash_multiset objects is based on a pairwise comparison between their elements. Two hash_multisets are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
### Example  
  
```  
// hashset_op_ne.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   using namespace stdext;  
   hash_multiset <int> hs1, hs2, hs3;  
   int i;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      hs1.insert ( i );  
      hs2.insert ( i * i );  
      hs3.insert ( i );  
   }  
  
   if ( hs1 != hs2 )  
      cout << "The hash_multisets hs1 and hs2 are not equal." << endl;  
   else  
      cout << "The hash_multisets hs1 and hs2 are equal." << endl;  
  
   if ( hs1 != hs3 )  
      cout << "The hash_multisets hs1 and hs3 are not equal." << endl;  
   else  
      cout << "The hash_multisets hs1 and hs3 are equal." << endl;  
}  
```  
  
  **The hash_multisets hs1 and hs2 are not equal.**  
**The hash_multisets hs1 and hs3 are equal.**    
##  <a name="operator_eq_eq__hash_multiset_"></a>  operator== (hash_multiset)  
  
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Tests if the hash_multiset object on the left side of the operator is equal to the hash_multiset object on the right side.  
  
```  
bool operator!==(    const hash_multiset <Key, Traits, Allocator>&  _Left ,    const hash_multiset <Key, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `hash_multiset`.  
  
 `_Right`  
 An object of type `hash_multiset`.  
  
### Return Value  
 **true** if the hash_multiset on the left side of the operator is equal to the hash_multiset on the right side of the operator; otherwise **false**.  
  
### Remarks  
 The comparison between hash_multiset objects is based on a pairwise comparison of their elements. Two hash_multisets are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
### Example  
  
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
## See Also  
 [&lt;hash_set&gt;](../vs140/-hash_set-.md)