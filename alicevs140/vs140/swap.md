---
title: "swap"
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
ms.assetid: b471a2de-035e-4aff-b1c7-345d85d93972
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap
The first override exchanges the values of two objects. The second override exchanges the values between two arrays of objects.  
  
## Syntax  
  
```  
template<class Type>  
   void swap(  
      Type& _Left,   
      Type& _Right  
   );  
template<class Type, size_t N>  
   void swap(  
      Type (&_Left)[N],  
      Type (&_Right)[N]  
   );  
```  
  
#### Parameters  
 `_Left`  
 For the first override, the first object to have its contents exchanged. For the second override, the first array of objects to have its contents exchanged.  
  
 `_Right`  
 For the first override, the second object to have its contents exchanged. For the second override, the second array of objects to have its contents exchanged.  
  
## Remarks  
 The first overload is designed to operate on individual objects. The second overload swaps the contents of objects between two arrays.  
  
## Example  
  
```  
// alg_swap.cpp  
// compile with: /EHsc  
#include <vector>  
#include <algorithm>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   vector <int> v1, v2;  
   vector <int>::iterator Iter1, Iter2, result;  
  
   for ( int i = 0 ; i <= 10 ; i++ )  
   {  
      v1.push_back( i );  
   }  
  
   for ( int ii = 0 ; ii <= 4 ; ii++ )  
   {  
      v2.push_back( 5 );  
   }  
  
   cout << "Vector v1 is ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")." << endl;  
  
   cout << "Vector v2 is ( " ;  
   for ( Iter2 = v2.begin( ) ; Iter2 != v2.end( ) ; Iter2++ )  
      cout << *Iter2 << " ";  
   cout << ")." << endl;  
  
   swap( v1, v2 );  
  
   cout << "Vector v1 is ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")." << endl;  
  
   cout << "Vector v2 is ( " ;  
   for ( Iter2 = v2.begin( ) ; Iter2 != v2.end( ) ; Iter2++ )  
      cout << *Iter2 << " ";  
   cout << ")." << endl;  
}  
```  
  
 **Vector v1 is ( 0 1 2 3 4 5 6 7 8 9 10 ).**  
**Vector v2 is ( 5 5 5 5 5 ).**  
**Vector v1 is ( 5 5 5 5 5 ).**  
**Vector v2 is ( 0 1 2 3 4 5 6 7 8 9 10 ).**   
## Requirements  
 **Header:** <algorithm\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)