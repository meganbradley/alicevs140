---
title: "max"
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
ms.assetid: 342d6303-fac9-46f2-a7f2-3a8c3c048cd6
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# max
Compares two objects and returns the larger of the two, where the ordering criterion may be specified by a binary predicate.  
  
## Syntax  
  
```  
template<class Type>  
    const Type& max(  
        const Type& _Left,   
        const Type& _Right  
    );  
template<class Type, class Pr>  
    const Type& max(  
        const Type& _Left,   
        const Type& _Right,  
        BinaryPredicate _Comp  
    );  
template<class Type>   
    Type& max (  
        initializer_list<Type> _Ilist  
    );  
template<class Type, class Pr>   
    Type& max(  
        initializer_list<Type> _Ilist,   
        BinaryPredicate _Comp  
    );  
```  
  
#### Parameters  
 `_Left`  
 The first of the two objects being compared.  
  
 `_Right`  
 The second of the two objects being compared.  
  
 `_Comp`  
 A binary predicate used to compare the two objects.  
  
 `_IList`  
 The initializer list that contains the objects to be compared.  
  
## Return Value  
 The greater of the two objects, unless neither is greater; in that case, it returns the first of the two objects. In the case of an initializer_list, it returns the greatest of the objects in the list.  
  
## Remarks  
 The `max` algorithm is unusual in having objects passed as parameters. Most Standard Template Library algorithms operate on a range of elements whose position is specified by iterators passed as parameters. If you need a function that operates on a range of elements, use [max_element](../vs140/max_element.md) instead.  
  
## Example  
  
```  
// alg_max.cpp  
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
   CInt&   operator=( const CInt& rhs ) {m_nVal =   
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
  
// Return whether absolute value of elem1 is greater than   
// absolute value of elem2  
bool abs_greater ( int elem1, int elem2 )  
{  
   if ( elem1 < 0 )   
      elem1 = -elem1;  
   if ( elem2 < 0 )   
      elem2 = -elem2;  
   return elem1 < elem2;  
};  
  
int main( )  
{  
   int a = 6, b = -7;  
   // Return the integer with the larger absolute value  
   const int& result1 = max(a, b, abs_greater);  
   // Return the larger integer  
   const int& result2 = max(a, b);  
  
   cout << "Using integers 6 and -7..." << endl;  
   cout << "The integer with the greater absolute value is: "   
        << result1 << "." << endl;  
   cout << "The integer with the greater value is: "   
        << result2 << "." << endl;  
   cout << endl;  
  
// Comparing the members of an initializer_list  
const int& result3 = max({ a, b });  
const int& result4 = max({ a, b }, abs_greater);  
  
cout << "Comparing the members of an initializer_list..." << endl;  
cout << "The member with the greater value is: " << result3 << endl;  
cout << "The integer with the greater absolute value is: " << result4 << endl;  
  
   // Comparing set containers with elements of type CInt   
   // using the max algorithm  
   CInt c1 = 1, c2 = 2, c3 = 3;  
   set<CInt> s1, s2, s3;  
   set<CInt>::iterator s1_Iter, s2_Iter, s3_Iter;  
  
   s1.insert ( c1 );  
   s1.insert ( c2 );  
   s2.insert ( c2 );  
   s2.insert ( c3 );  
  
   cout << "s1 = (";  
   for ( s1_Iter = s1.begin( ); s1_Iter != --s1.end( ); s1_Iter++ )  
      cout << " " << *s1_Iter << ",";  
   s1_Iter = --s1.end( );  
   cout << " " << *s1_Iter << " )." << endl;  
  
   cout << "s2 = (";  
   for ( s2_Iter = s2.begin( ); s2_Iter != --s2.end( ); s2_Iter++ )  
      cout << " " << *s2_Iter << ",";  
   s2_Iter = --s2.end( );  
   cout << " " << *s2_Iter << " )." << endl;  
  
   s3 = max ( s1, s2 );  
   cout << "s3 = max ( s1, s2 ) = (";  
   for ( s3_Iter = s3.begin( ); s3_Iter != --s3.end( ); s3_Iter++ )  
      cout << " " << *s3_Iter << ",";  
   s3_Iter = --s3.end( );  
   cout << " " << *s3_Iter << " )." << endl << endl;  
  
   // Comparing vectors with integer elements using the max algorithm  
   vector <int> v1, v2, v3, v4, v5;  
   vector <int>::iterator Iter1, Iter2, Iter3, Iter4, Iter5;  
  
   int i;  
   for ( i = 0 ; i <= 2 ; i++ )  
   {  
      v1.push_back( i );  
   }  
  
   int ii;  
   for ( ii = 0 ; ii <= 2 ; ii++ )  
   {  
      v2.push_back( ii );  
   }  
  
   int iii;  
   for ( iii = 0 ; iii <= 2 ; iii++ )  
   {  
      v3.push_back( 2 * iii );  
   }  
  
   cout << "Vector v1 is ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")." << endl;  
  
   cout << "Vector v2 is ( " ;  
   for ( Iter2 = v2.begin( ) ; Iter2 != v2.end( ) ; Iter2++ )  
      cout << *Iter2 << " ";  
   cout << ")." << endl;  
  
   cout << "Vector v3 is ( " ;  
   for ( Iter3 = v3.begin( ) ; Iter3 != v3.end( ) ; Iter3++ )  
      cout << *Iter3 << " ";  
   cout << ")." << endl;  
  
   v4 = max ( v1, v2 );  
   v5 = max ( v1, v3 );  
  
   cout << "Vector v4 = max (v1,v2) is ( " ;  
   for ( Iter4 = v4.begin( ) ; Iter4 != v4.end( ) ; Iter4++ )  
      cout << *Iter4 << " ";  
   cout << ")." << endl;  
  
   cout << "Vector v5 = max (v1,v3) is ( " ;  
   for ( Iter5 = v5.begin( ) ; Iter5 != v5.end( ) ; Iter5++ )  
      cout << *Iter5 << " ";  
   cout << ")." << endl;  
}  
```  
  
 **Using integers 6 and -7...**  
**The integer with the greater absolute value is: -7**  
**The integer with the greater value is: 6.**  
**Comparing the members of an initializer_list...The member with the greater value is: 6The integer wiht the greater absolute value is: -7**  
**s1 = ( CInt( 1 ), CInt( 2 ) ).**  
**s2 = ( CInt( 2 ), CInt( 3 ) ).**  
**s3 = max ( s1, s2 ) = ( CInt( 2 ), CInt( 3 ) ).**  
**Vector v1 is ( 0 1 2 ).**  
**Vector v2 is ( 0 1 2 ).**  
**Vector v3 is ( 0 2 4 ).**  
**Vector v4 = max (v1,v2) is ( 0 1 2 ).**  
**Vector v5 = max (v1,v3) is ( 0 2 4 ).**   
## Requirements  
 **Header:** <algorithm\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)