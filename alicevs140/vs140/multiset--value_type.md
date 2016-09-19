---
title: "multiset::value_type"
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
ms.assetid: a514b43d-4f70-42d2-b610-e53139a45387
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::value_type
A type that describes an object stored as an element as a multiset in its capacity as a value.  
  
## Syntax  
  
```  
typedef Key value_type;  
```  
  
## Remarks  
 `value_type` is a synonym for the template parameter `Key`.  
  
 Note that both [key_type](../vs140/multiset--key_type.md) and `value_type` are synonyms for the template parameter **Key**. Both types are provided for the classes set and multiset, where they are identical, for compatibility with the classes map and multimap, where they are distinct.  
  
 For more information on `Key`, see the Remarks section of the topic.  
  
## Example  
  
```  
// multiset_value_type.cpp  
// compile with: /EHsc  
#include <set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   multiset <int> ms1;  
   multiset <int>::iterator ms1_Iter;  
  
   multiset <int> :: value_type svt_Int;   // Declare value_type  
   svt_Int = 10;             // Initialize value_type  
  
   multiset <int> :: key_type skt_Int;   // Declare key_type  
   skt_Int = 20;             // Initialize key_type  
  
   ms1.insert( svt_Int );         // Insert value into s1  
   ms1.insert( skt_Int );         // Insert key into s1  
  
   // A multiset accepts key_types or value_types as elements  
   cout << "The multiset has elements:";  
   for ( ms1_Iter = ms1.begin( ) ; ms1_Iter != ms1.end( ); ms1_Iter++ )  
      cout << " " << *ms1_Iter;  
   cout << "." << endl;  
}  
```  
  
 **The multiset has elements: 10 20.**   
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [multiset Class](../vs140/multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)