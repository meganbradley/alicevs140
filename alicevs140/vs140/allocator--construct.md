---
title: "allocator::construct"
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
ms.assetid: 4155f804-02b8-44c0-b5ee-e31287e2c328
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# allocator::construct
Constructs a specific type of object at a specified address that is initialized with a specified value.  
  
## Syntax  
  
```  
  
      void construct(  
   pointer _Ptr,   
   const Type& _Val  
);void construct(  
   pointer _Ptr,   
   Type&& _Val  
);  
template<class _Other>  
    void construct(  
        pointer _Ptr,   
        _Other&&... _Val  
    );  
```  
  
#### Parameters  
 `_Ptr`  
 A pointer to the location where the object is to be constructed.  
  
 `_Val`  
 The value with which the object being constructed is to be initialized.  
  
## Remarks  
 The first member function is equivalent to **new** ( (`void` \*) `_Ptr` ) **Type** ( `_Val` ).  
  
## Example  
  
```  
// allocator_construct.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <algorithm>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   vector <int> v1;  
   vector <int>::iterator v1Iter;  
   vector <int>:: allocator_type v1Alloc;  
  
   int i;  
   for ( i = 1 ; i <= 7 ; i++ )  
   {  
      v1.push_back( 3 * i );  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
  
   allocator<int>::pointer v1PtrA;  
   int kA = 6, kB = 7;  
   v1PtrA = v1Alloc.address( *find( v1.begin( ), v1.end( ), kA ) );  
   v1Alloc.destroy ( v1PtrA );  
   v1Alloc.construct ( v1PtrA , kB );  
  
   cout << "The modified vector v1 is:\n ( " ;  
   for ( v1Iter = v1.begin( ) ; v1Iter != v1.end( ) ; v1Iter++ )  
      cout << *v1Iter << " ";  
   cout << ")." << endl;  
}  
```  
  
 **The original vector v1 is:**  
 **( 3 6 9 12 15 18 21 ).**  
**The modified vector v1 is:**  
 **( 3 7 9 12 15 18 21 ).**   
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [allocator Class](../vs140/allocator-Class.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [Lvalue Reference Declarator: &](../vs140/Lvalue-Reference-Declarator---.md)   
 [Rvalue Reference Declarator: &&](../vs140/Rvalue-Reference-Declarator----.md)