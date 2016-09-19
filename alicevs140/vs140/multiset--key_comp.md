---
title: "multiset::key_comp"
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
ms.assetid: 490a2540-a186-49b7-b92b-b944596a46d3
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::key_comp
Retrieves a copy of the comparison object used to order keys in a multiset.  
  
## Syntax  
  
```  
  
key_compare key_comp( ) const;  
  
```  
  
## Return Value  
 Returns the function object that a multiset uses to order its elements, which is the template parameter `Compare`.  
  
 For more information on `Compare`, see the Remarks section of the [multiset Class](../vs140/multiset-Class.md) topic.  
  
## Remarks  
 The stored object defines the member function:  
  
 **bool operator**(**const Key&** *x*, **const Key&** *y*);  
  
 which returns true if *x* strictly precedes *y* in the sort order.  
  
 Note that both [key_compare](../vs140/multiset--key_compare.md) and [value_compare](../vs140/multiset--value_compare.md) are synonyms for the template parameter `Compare`. Both types are provided for the classes set and multiset, where they are identical, for compatibility with the classes map and multimap, where they are distinct.  
  
## Example  
  
```  
// multiset_key_comp.cpp  
// compile with: /EHsc  
#include <set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   multiset <int, less<int> > ms1;  
   multiset <int, less<int> >::key_compare kc1 = ms1.key_comp( ) ;  
   bool result1 = kc1( 2, 3 ) ;  
   if( result1 == true )     
   {  
      cout << "kc1( 2,3 ) returns value of true, "  
           << "where kc1 is the function object of s1."  
           << endl;  
   }  
   else     
   {  
      cout << "kc1( 2,3 ) returns value of false "  
           << "where kc1 is the function object of ms1."  
           << endl;  
   }  
  
   multiset <int, greater<int> > ms2;  
   multiset <int, greater<int> >::key_compare kc2 = ms2.key_comp( ) ;  
   bool result2 = kc2( 2, 3 ) ;  
   if( result2 == true )     
   {  
      cout << "kc2( 2,3 ) returns value of true, "  
           << "where kc2 is the function object of ms2."  
           << endl;  
   }  
   else     
   {  
      cout << "kc2( 2,3 ) returns value of false, "  
           << "where kc2 is the function object of ms2."  
           << endl;  
   }  
}  
```  
  
 **kc1( 2,3 ) returns value of true, where kc1 is the function object of s1.**  
**kc2( 2,3 ) returns value of false, where kc2 is the function object of ms2.**   
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [multiset Class](../vs140/multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)