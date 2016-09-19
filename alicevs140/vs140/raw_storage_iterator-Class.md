---
title: "raw_storage_iterator Class"
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
ms.assetid: 6f033f15-f48e-452a-a326-647ea2cf346f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# raw_storage_iterator Class
An adaptor class that is provided to enable algorithms to store their results into uninitialized memory.  
  
## Syntax  
  
```  
template <class  OutputIterator,  class  Type> class raw_storage_iterator  
  
```  
  
#### Parameters  
 `OutputIterator`  
 Specifies the output iterator for the object being stored.  
  
 *Type*  
 The type of object for which storage is being allocated.  
  
## Remarks  
 The class describes an output iterator that constructs objects of type **Type** in the sequence it generates. An object of class `raw_storage_iterator`< **ForwardIterator**, **Type**> accesses storage through a forward iterator object, of class **ForwardIterator**, that you specify when you construct the object. For an object first of class **ForwardIterator**, the expression **&\*first** must designate unconstructed storage for the next object (of type **Type**) in the generated sequence.  
  
 This adaptor class is used when it is necessary to separate memory allocation and object construction. The `raw_storage_iterator` can be used to copy objects into uninitialized storage, such as memory allocated using the `malloc` function.  
  
## Members  
  
### Constructors  
  
|||  
|-|-|  
|[raw_storage_iterator](#raw_storage_iterator__raw_storage_iterator)|Constructs a raw storage iterator with a specified underlying output iterator.|  
  
### Typedefs  
  
|||  
|-|-|  
|[element_type](#raw_storage_iterator__element_type)|Provides a type that describes an element to be stored a raw storage iterator.|  
|[iter_type](#raw_storage_iterator__iter_type)|Provides a type that describes an iterator that underlies a raw storage iterator.|  
  
### Operators  
  
|||  
|-|-|  
|[operator*](#raw_storage_iterator__operator_star)|A dereferencing operator used to implement the output iterator expression * `ii` = `x`.|  
|[operator=](#raw_storage_iterator__operator_eq)|An assignment operator used to implement the raw storage iterator expression * `i` = `x` for storing in memory.|  
|[operator++](#raw_storage_iterator__operator_add_add)|Preincrement and postincrement operators for raw storage iterators.|  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
##  <a name="raw_storage_iterator__element_type"></a>  raw_storage_iterator::element_type  
 Provides a type that describes an element to be stored a raw storage iterator.  
  
```  
typedef Type element _ type;  
  
```  
  
### Remarks  
 The type is a synonym for the raw_storage_iterator class template parameter **Type**.  
  
##  <a name="raw_storage_iterator__iter_type"></a>  raw_storage_iterator::iter_type  
 Provides a type that describes an iterator that underlies a raw storage iterator.  
  
```  
typedef ForwardIterator iter_type;  
```  
  
### Remarks  
 The type is a synonym for the template parameter **ForwardIterator**.  
  
##  <a name="raw_storage_iterator__operator_star"></a>  raw_storage_iterator::operator*  
 A dereferencing operator used to implement the raw storage iterator expression \*                *ii* =                 *x*.  
  
```  
raw_storage_iterator<ForwardIterator, Type>& operator*( );  
```  
  
### Return Value  
 A reference to the raw storage iterator  
  
### Remarks  
 The requirements for a **ForwardIterator** are that the raw storage iterator must satisfy require only the expression \*                        *ii* =                         *t* be valid and that it says nothing about the **operator** or the `operator=` on their own. The member operators in this implementation returns **\*this**, so that [operator=](#raw_storage_iterator__operator_eq)( **constType**&) can perform the actual store in an expression, such as \*                        *_Ptr* = `_Val`.  
  
### Example  
  
```  
// raw_storage_iterator_op_deref.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iterator>  
#include <memory>  
#include <list>  
using namespace std;  
  
class Int   
{  
public:  
   Int(int i)   
   {  
      cout << "Constructing " << i << endl;   
      x = i;  
      bIsConstructed = true;  
   };  
  
   Int &operator=(int i)   
   {  
      if (!bIsConstructed)  
         cout << "Not constructed.\n";  
      cout << "Copying " << i << endl;    
      x = i;   
      return *this;  
   };  
  
   int x;  
  
private:  
   bool bIsConstructed;  
};  
  
int main( void)   
{  
   Int *pInt = ( Int* ) malloc( sizeof( Int ) );  
   memset( pInt, 0, sizeof( Int ) ); // Set bIsConstructed to false;  
   *pInt = 5;  
   raw_storage_iterator< Int*, Int > it( pInt );  
   *it = 5;  
}  
\* Output:   
Not constructed.  
Copying 5  
Constructing 5  
*\  
```  
  
##  <a name="raw_storage_iterator__operator_eq"></a>  raw_storage_iterator::operator=  
 Assignment operator used to implement the raw storage iterator expression \*                *i* =                 *x* for storing in memory.  
  
```  
raw_storage_iterator<ForwardIterator, Type>& operator=(  
   const Type& _Val  
);  
```  
  
### Parameters  
 `_Val`  
 The value of the object of type **Type** to be inserted into memory.  
  
### Return Value  
 The operator inserts `_Val` into memory, and then returns a reference to the raw storage iterator.  
  
### Remarks  
 The requirements for a **ForwardIterator** state that the raw storage iterator must satisfy require only the expression \*                        *ii* =                         *t* be valid, and that it says nothing about the **operator** or the `operator=` on their own. These member operators return **\*this**.  
  
 The assignment operator constructs the next object in the output sequence using the stored iterator value first, by evaluating the placement new expression **new** ( ( `void` \*)&\* **first**) **Type**( `_Val`).  
  
### Example  
  
```  
// raw_storage_iterator_op_assign.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iterator>  
#include <memory>  
#include <list>  
using namespace std;  
  
class Int   
{  
public:  
   Int( int i )   
   {  
      cout << "Constructing " << i << endl;   
      x = i;  
      bIsConstructed = true;  
   };  
   Int &operator=( int i )   
   {  
      if ( !bIsConstructed )  
         cout << "Not constructed.\n";  
      cout << "Copying " << i << endl; x = i;  
      return *this;  
   };  
   int x;  
private:  
   bool bIsConstructed;  
};  
  
int main( void )  
{  
   Int *pInt = ( Int* )malloc( sizeof( Int ) );  
   memset( pInt, 0, sizeof( Int ) ); // Set bIsConstructed to false;  
  
   *pInt = 5;  
  
   raw_storage_iterator<Int*, Int> it( pInt );  
   *it = 5;  
}  
\* Output:   
Not constructed.  
Copying 5  
Constructing 5  
*\  
```  
  
##  <a name="raw_storage_iterator__operator_add_add"></a>  raw_storage_iterator::operator++  
 Preincrement and postincrement operators for raw storage iterators.  
  
```  
raw_storage_iterator<ForwardIterator, Type>& operator++( );  
raw_storage_iterator<ForwardIterator, Type> operator++(int);  
```  
  
### Return Value  
 An raw storage iterator or a reference to an raw storage iterator.  
  
### Remarks  
 The first operator eventually attempts to extract and store an object of type **CharType** from the associated input stream. The second operator makes a copy of the object, increments the object, and then returns the copy.  
  
 The first preincrement operator increments the stored output iterator object, and then returns **\*this**.  
  
 The second postincrement operator makes a copy of **\*this**, increments the stored output iterator object, and then returns the copy.  
  
 The constructor stores **first** as the output iterator object.  
  
### Example  
  
```  
// raw_storage_iterator_op_incr.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iterator>  
#include <memory>  
#include <list>  
using namespace std;  
  
int main( void )  
{  
   int *pInt = new int[5];  
   std::raw_storage_iterator<int*,int> it( pInt );  
   for ( int i = 0; i < 5; i++, it++ ) {  
      *it = 2 * i;  
};  
  
   for ( int i = 0; i < 5; i++ ) cout << "array " << i << " = " << pInt[i] << endl;;  
  
   delete[] pInt;  
}  
\* Output:   
array 0 = 0  
array 1 = 2  
array 2 = 4  
array 3 = 6  
array 4 = 8  
*\  
```  
  
##  <a name="raw_storage_iterator__raw_storage_iterator"></a>  raw_storage_iterator::raw_storage_iterator  
 Constructs a raw storage iterator with a specified underlying output iterator.  
  
```  
explicit raw_storage_iterator(  
   ForwardIterator _First  
);  
```  
  
### Parameters  
 `_First`  
 The forward iterator that is to underlie the `raw_storage_iterator` object being constructed.  
  
### Example  
  
```  
// raw_storage_iterator_ctor.cpp  
// compile with: /EHsc /W3  
#include <iostream>  
#include <iterator>  
#include <memory>  
#include <list>  
using namespace std;  
  
class Int  
{  
public:  
   Int(int i)  
   {  
      cout << "Constructing " << i << endl;  
      x = i;  
      bIsConstructed = true;  
   };  
   Int &operator=( int i )  
   {  
      if (!bIsConstructed)  
         cout << "Error! I'm not constructed!\n";  
      cout << "Copying " << i << endl;  x = i; return *this;  
   };  
   int x;  
   bool bIsConstructed;  
};  
  
int main( void )  
{  
   std::list<int> l;  
   l.push_back( 1 );  
   l.push_back( 2 );  
   l.push_back( 3 );  
   l.push_back( 4 );  
  
   Int *pInt = (Int*)malloc(sizeof(Int)*l.size( ));  
   memset (pInt, 0, sizeof(Int)*l.size( ));  
   // Hack: make sure bIsConstructed is false  
  
   std::copy( l.begin( ), l.end( ), pInt );  // C4996  
   for (unsigned int i = 0; i < l.size( ); i++)  
      cout << "array " << i << " = " << pInt[i].x << endl;;  
  
   memset (pInt, 0, sizeof(Int)*l.size( ));  
   // hack: make sure bIsConstructed is false  
  
   std::copy( l.begin( ), l.end( ),  
      std::raw_storage_iterator<Int*,Int>(pInt));  // C4996  
   for (unsigned int i = 0; i < l.size( ); i++ )  
      cout << "array " << i << " = " << pInt[i].x << endl;  
  
   free(pInt);  
}  
\* Output:   
Error! I'm not constructed!  
Copying 1  
Error! I'm not constructed!  
Copying 2  
Error! I'm not constructed!  
Copying 3  
Error! I'm not constructed!  
Copying 4  
array 0 = 1  
array 1 = 2  
array 2 = 3  
array 3 = 4  
Constructing 1  
Constructing 2  
Constructing 3  
Constructing 4  
array 0 = 1  
array 1 = 2  
array 2 = 3  
array 3 = 4  
*\  
```  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)