---
title: "min"
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
ms.assetid: 636d6d14-3957-43c0-a197-653afa45e2d7
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# min
Compares two objects and returns the lesser of the two, where the ordering criterion may be specified by a binary predicate.  
  
## Syntax  
  
```  
template<class Type>  
    const Type& min(  
        const Type& _Left,   
        const Type& _Right  
    );  
template<class Type, class Pr>  
    const Type& min(  
        const Type& _Left,   
        const Type& _Right,  
        BinaryPredicate _Comp  
    );  
template<class Type>   
    Type min ( initializer_list<Type> _Ilist  
    );  
template<class Type, class Pr>    Type min (  
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
 The initializer_list that contains the members to be compared.  
  
## Return Value  
 The lesser of the two objects, unless neither is lesser; in that case, it returns the first of the two objects. In the case of an initializer_list, it returns the least of the objects in the list.  
  
## Remarks  
 The `min` algorithm is unusual in having objects passed as parameters. Most Standard Template Library algorithms operate on a range of elements whose position is specified by iterators passed as parameters. If you need a function that uses a range of elements, use [min_element](../vs140/min_element.md).  
  
## Example  
  
```  
// alg_min.cpp  
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
    friend ostream& operator<<(ostream& osIn, const CInt& rhs);  
  
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
  
int main( )  
{  
    // Comparing integers directly using the min algorithm with  
    // binary predicate mod_lesser & with default less than  
    int a = 6, b = -7, c = 7 ;  
    const int& result1 = min ( a, b, mod_lesser );  
    const int& result2 = min ( b, c );  
  
    cout << "The mod_lesser of the integers 6 & -7 is: "   
        << result1 << "." << endl;  
     cout << "The lesser of the integers -7 & 7 is: "   
        << result2 << "." << endl;  
    cout << endl;  
  
// Comparing the members of an initializer_list  
    const int& result3 = min({ a, c });  
    const int& result4 = min({ a, b }, mod_lesser);  
  
    cout << "The lesser of the integers 6 & 7 is: "  
        << result3 << "." << endl;  
    cout << "The mod_lesser of the integers 6 & -7 is: "  
        << result4 << "." << endl;  
    cout << endl;  
  
    // Comparing set containers with elements of type CInt   
       // using the min algorithm  
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
  
    s3 = min ( s1, s2 );  
    cout << "s3 = min ( s1, s2 ) = (";  
    for ( s3_Iter = s3.begin( ); s3_Iter != --s3.end( ); s3_Iter++ )  
        cout << " " << *s3_Iter << ",";  
    s3_Iter = --s3.end( );  
    cout << " " << *s3_Iter << " )." << endl << endl;  
  
    // Comparing vectors with integer elements using min algorithm  
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
  
    v4 = min ( v1, v2 );  
    v5 = min ( v1, v3 );  
  
    cout << "Vector v4 = min ( v1,v2 ) is ( " ;  
    for ( Iter4 = v4.begin( ) ; Iter4 != v4.end( ) ; Iter4++ )  
        cout << *Iter4 << " ";  
    cout << ")." << endl;  
  
    cout << "Vector v5 = min ( v1,v3 ) is ( " ;  
    for ( Iter5 = v5.begin( ) ; Iter5 != v5.end( ) ; Iter5++ )  
        cout << *Iter5 << " ";  
    cout << ")." << endl;  
}  
```  
  
 **The mod_lesser of the integers 6 & -7 is: 6.**  
**The lesser of the integers -7 & 7 is: -7.**  
**The lesser of the integers 6 & 7 is: 6.The mod_lesser of the integers 6 & -7 is: 6.**  
**s1 = ( CInt( 1 ), CInt( 2 ) ).**  
**s2 = ( CInt( 2 ), CInt( 3 ) ).**  
**s3 = min ( s1, s2 ) = ( CInt( 1 ), CInt( 2 ) ).**  
**Vector v1 is ( 0 1 2 ).**  
**Vector v2 is ( 0 1 2 ).**  
**Vector v3 is ( 0 2 4 ).**  
**Vector v4 = min ( v1,v2 ) is ( 0 1 2 ).**  
**Vector v5 = min ( v1,v3 ) is ( 0 1 2 ).**   
## Requirements  
 **Header:** <algorithm\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)