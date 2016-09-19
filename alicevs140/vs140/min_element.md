---
title: "min_element"
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
ms.assetid: 4cf188f9-59f6-4d2c-a1aa-a259c0b1ac6c
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# min_element
Finds the first occurrence of smallest element in a specified range where the ordering criterion may be specified by a binary predicate.  
  
## Syntax  
  
```  
  
      template<class ForwardIterator>  
   ForwardIterator min_element(  
      ForwardIterator first,   
      ForwardIterator last  
   );  
template<class ForwardIterator, class BinaryPredicate>  
   ForwardIterator min_element(  
      ForwardIterator first,   
      ForwardIterator last,  
      BinaryPredicate comp  
   );  
```  
  
#### Parameters  
 `first`  
 A forward iterator addressing the position of the first element in the range to be searched for the smallest element.  
  
 `last`  
 A forward iterator addressing the position one past the final element in the range to be searched for the smallest element.  
  
 `comp`  
 User-defined predicate function object that defines the sense in which one element is greater than another. The binary predicate takes two arguments and should return **true** when the first element is less than the second element and **false** otherwise.  
  
## Return Value  
 A forward iterator addressing the position of the first occurrence of the smallest element in the range searched.  
  
## Remarks  
 The range referenced must be valid; all pointers must be dereferenceable and within each sequence the last position is reachable from the first by incrementation.  
  
 The complexity is linear: (`last` – `first`) – 1 comparisons are required for a nonempty range.  
  
## Example  
  
```  
// alg_min_element.cpp  
// compile with: /EHsc  
#include <vector>  
#include <set>  
#include <algorithm>  
#include <iostream>  
#include <ostream>  
  
using namespace std;  
class CInt;  
ostream& operator<<( ostream& osIn, const CInt& rhs );  
  
class CInt  
{  
public:  
   CInt( int n = 0 ) : m_nVal( n ){}  
   CInt( const CInt& rhs ) : m_nVal( rhs.m_nVal ){}  
   CInt& operator=( const CInt& rhs ) {m_nVal =   
   rhs.m_nVal; return *this;}  
   bool operator<( const CInt& rhs ) const   
      {return ( m_nVal < rhs.m_nVal );}  
   friend ostream& operator<<( ostream& osIn, const CInt& rhs );  
  
private:  
   int m_nVal;  
};  
  
inline ostream& operator<<( ostream& osIn, const CInt& rhs )  
{  
   osIn << "CInt( " << rhs.m_nVal << " )";   
   return osIn;  
}  
  
// Return whether modulus of elem1 is less than modulus of elem2  
bool mod_lesser ( int elem1, int elem2 )  
{  
   if ( elem1 < 0 )   
      elem1 = - elem1;  
   if ( elem2 < 0 )   
      elem2 = - elem2;  
   return elem1 < elem2;  
};  
  
int main()  
{  
   // Searching a set container with elements of type CInt   
   // for the minimum element   
   CInt c1 = 1, c2 = 2, c3 = -3;  
   set<CInt> s1;  
   set<CInt>::iterator s1_Iter, s1_R1_Iter, s1_R2_Iter;  
  
   s1.insert ( c1 );  
   s1.insert ( c2 );  
   s1.insert ( c3 );  
  
   cout << "s1 = (";  
   for ( s1_Iter = s1.begin( ); s1_Iter != --s1.end( ); s1_Iter++ )  
      cout << " " << *s1_Iter << ",";  
   s1_Iter = --s1.end( );  
   cout << " " << *s1_Iter << " )." << endl;  
  
   s1_R1_Iter = min_element ( s1.begin ( ) , s1.end ( ) );  
  
   cout << "The smallest element in s1 is: " << *s1_R1_Iter << endl;  
   cout << endl;  
  
   // Searching a vector with elements of type int for the maximum  
   // element under default less than & mod_lesser binary predicates  
   vector <int> v1;  
   vector <int>::iterator v1_Iter, v1_R1_Iter, v1_R2_Iter;  
  
   int i;  
   for ( i = 0 ; i <= 3 ; i++ )  
   {  
      v1.push_back( i );  
   }  
  
   int ii;  
   for ( ii = 1 ; ii <= 4 ; ii++ )  
   {  
      v1.push_back( - 2 * ii );  
   }  
  
   cout << "Vector v1 is ( " ;  
   for ( v1_Iter = v1.begin( ) ; v1_Iter != v1.end( ) ; v1_Iter++ )  
      cout << *v1_Iter << " ";  
   cout << ")." << endl;  
  
   v1_R1_Iter = min_element ( v1.begin ( ) , v1.end ( ) );  
   v1_R2_Iter = min_element ( v1.begin ( ) , v1.end ( ), mod_lesser);  
  
   cout << "The smallest element in v1 is: " << *v1_R1_Iter << endl;  
   cout << "The smallest element in v1 under the mod_lesser"  
        << "\n binary predicate is: " << *v1_R2_Iter << endl;  
}  
```  
  
 **s1 = ( CInt( -3 ), CInt( 1 ), CInt( 2 ) ).**  
**The smallest element in s1 is: CInt( -3 )**  
**Vector v1 is ( 0 1 2 3 -2 -4 -6 -8 ).**  
**The smallest element in v1 is: -8**  
**The smallest element in v1 under the mod_lesser**  
 **binary predicate is: 0**   
## Requirements  
 **Header:** <algorithm\>  
  
 **Namespace:** std  
  
## See Also  
 [min_element](../vs140/min_element--STL-Samples-.md)   
 [Predicate Version of min_element](../vs140/Predicate-Version-of-min_element.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)