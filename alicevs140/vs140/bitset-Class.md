---
title: "bitset Class"
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
ms.assetid: 28b86964-87b4-429c-8124-b6c251b6c50b
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bitset Class
Describes a type of object that stores a sequence consisting of a fixed number of bits that provide a compact way of keeping flags for a set of items or conditions. The bitset class supports operations on objects of type bitset that contain a collection of bits and provide constant-time access to each bit.  
  
## Syntax  
  
```  
  
template <size_t   
N  
>  
   class bitset  
  
```  
  
#### Parameters  
 *N*  
 Specifies the number of bits in the bitset object with a nonzero integer of type                         **size_t** that must be known at compile time.  
  
## Remarks  
 Unlike the similar                 [vector<bool\> Class](../vs140/vector-bool--Class.md), the bitset class does not have iterators and is not an Standard Template Library container. It also differs from vector<bool\> by being of some specific size that is fixed at compile time in accordance with the size specified by the template parameter                 **N** when the                 **bitset<N\>** is declared.  
  
 A bit is set if its value is 1 and reset if its value is 0. To flip or toggle a bit is to change its value from 1 to 0 or from 0 to 1. The                 **N** bits in a bitset are indexed by integer values from 0 to                 **N**Â -Â 1, where 0 indexes the first bit position and                 **N***Â* -Â 1 the final bit position.  
  
### Constructors  
  
|||  
|-|-|  
|[bitset](#bitset__bitset)|Constructs an object of class                                         `bitset<N>` and initializes the bits to zero, to some specified value, or to values obtained from characters in a string.|  
  
### Typedefs  
  
|||  
|-|-|  
|[element_type](#bitset__element_type)|A type that is a synonym for the data type                                         `bool` and can be used to reference element bits in a                                         `bitset`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[all](#bitset__all)|Tests all of the bits in this                                         `bitset` to determine whether they are all set to                                         `true`.|  
|[any](#bitset__any)|The member function tests whether any bit in the sequence is set to 1.|  
|[count](#bitset__count)|The member function returns the number of bits set in the bit sequence.|  
|[flip](#bitset__flip)|Toggles the value of all the bits in a                                         `bitset` or toggles a single bit at a specified position.|  
|[none](#bitset__none)|Tests if no bit has been set to 1 in a                                         `bitset` object.|  
|[reset](#bitset__reset)|Resets all the bits in a                                         `bitset` to 0 or resets a bit at a specified position to 0.|  
|[set](#bitset__set)|Sets all the bits in a                                         `bitset` to 1 or sets a bit at a specified position to 1.|  
|[size](#bitset__size)|Returns the number of bits in a                                         `bitset` object.|  
|[test](#bitset__test)|Tests whether the bit at a specified position in a                                         `bitset` is set to 1.|  
|[to_string](#bitset__to_string)|Converts a                                         `bitset` object to a string representation.|  
|[to_ullong](#bitset__to_ullong)|Returns the sum of the bit values in the                                         `bitset` as an                                         `unsigned long long`.|  
|[to_ulong](#bitset__to_ulong)|Converts a                                         `bitset` object to the                                         `unsigned long` that would generate the sequence of bits contained if used to initialize the                                         `bitset`.|  
  
### Member Classes  
  
|||  
|-|-|  
|[reference](#bitset__reference)|A proxy class that provides references to bits contained in a                                         `bitset` that is used to access and manipulate the individual bits as a helper class for the                                         `operator[]` of class                                         `bitset`.|  
  
### Operators  
  
|||  
|-|-|  
|[operator!=](#bitset__operator_neq)|Tests a target                                         `bitset` for inequality with a specified                                         `bitset`.|  
|[operator&=](#bitset__operator_amp__eq)|Performs a bitwise combination of bitsets with the logical                                         `AND` operation.|  
|[operator<<](#bitset__operator_lt__lt_)|Shifts the bits in a                                         `bitset` to the left a specified number of positions and returns the result to a new                                         `bitset`.|  
|[operator<<=](#bitset__operator_lt__lt__eq)|Shifts the bits in a                                         `bitset` to the left a specified number of positions and returns the result to the targeted                                         `bitset`.|  
|[operator==](#bitset__operator_eq_eq)|Tests a target                                         `bitset` for equality with a specified                                         `bitset`.|  
|[operator>>](#bitset__operator_gt__gt_)|Shifts the bits in a                                         `bitset` to the right a specified number of positions and returns the result to a new                                         `bitset`.|  
|[operator>>=](#bitset__operator_gt__gt__eq)|Shifts the bits in a                                         `bitset` to the right a specified number of positions and returns the result to the targeted                                         `bitset`.|  
|[operator&#91;&#93;](#bitset__operator_at)|Returns a reference to a bit at a specified position in a                                         `bitset` if the                                         `bitset` is modifiable; otherwise, it returns the value of the bit at that position.|  
|[operator^=](#bitset__operator_xor_eq)|Performs a bitwise combination of bitsets with the exclusive                                         `OR` operation.|  
|[operator&#124;=](#bitset__operator_or_eq')|Performs a bitwise combination of bitsets with the inclusive                                         `OR` operation.|  
|[operator~](#bitset__operator_dtor)|Toggles all the bits in a target                                         `bitset` and returns the result.|  
  
## Requirements  
 **Header:** <bitset\>  
  
 **Namespace:** std  
  
##  <a name="bitset__all"></a>  bitset::all  
 Tests all of the bits in this bitset to determine if they are all set to true.  
  
```  
  
bool all() const;  
  
```  
  
### Return Value  
 Returns true if all bits in this set are true. Returns                         **false** if one or more bits are false.  
  
##  <a name="bitset__any"></a>  bitset::any  
 Tests whether any bit in the sequence is set to 1.  
  
```  
  
bool any( ) const;  
  
```  
  
### Return Value  
 **true** if any bit in the bitset is set to 1;                         **false** if all the bits are 0.  
  
### Example  
  
```  
// bitset_any.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 6 );  
   bool b, rb;  
  
   cout << "The original bitset b1( 6 ) is: ( "<< b1 << " )"  
        << endl;  
  
   b = b1.any ( );  
  
   if ( b )  
      cout << "At least one of the bits in bitset is set to 1."  
           << endl;  
   else  
      cout << "None of the bits in bitset are set to 1."  
           << endl;  
  
   bitset<5> rb1;  
   rb1 = b1.reset ( );  
  
   cout << "The reset bitset is: ( "<< b1 << " )"  
        << endl;  
  
   rb = rb1.any ( );  
  
   if ( rb )  
      cout << "At least one of the bits in the reset bitset "  
           << "are set to 1." << endl;  
   else  
      cout << "None of the bits in bitset b1 are set to 1."  
           << endl;  
}  
```  
  
  **The original bitset b1( 6 ) is: ( 00110 )**  
**At least one of the bits in bitset is set to 1.**  
**The reset bitset is: ( 00000 )**  
**None of the bits in bitset b1 are set to 1.**    
##  <a name="bitset__bitset"></a>  bitset::bitset  
 Constructs an object of class                 `bitset<N>` and initializes the bits to zero, or to some specified value, or to values obtained from characters in a string.  
  
```  
bitset( );  
bitset(  
   unsigned long long                 _Val  
);  
explicit bitset(  
   const char *                 _CStr  
);   
template<   
  class CharType,   
  class Traits,   
  class Allocator   
>  
  explicit bitset(  
    const basic_string< CharType, Traits, Allocator >&                 _Str,  
    typename basic_string<   
      CharType, Traits, Allocator >::size_type                 _Pos = 0  
  );  
template<  
  class CharType,  
  class Traits,  
  class Allocator   
>  
 explicit bitset(  
  const basic_string< CharType, Traits, Allocator >&                 _Str,  
  typename basic_string<  
    CharType, Traits, Allocator >::size_type                 _Pos,  
  typename basic_string<   
    CharType, Traits, Allocator >::size_type                 _Count,  
  CharType                 _Zero = CharType (â€™0â€™),   
  CharType                 _One  = CharType (â€™1â€™)  
);  
```  
  
### Parameters  
 `_Val`  
 The unsigned integer whose base two representation is used to initialize the bits in the bitset being constructed.  
  
 `_Str`  
 The string of zeros and ones used to initialize the bitset bit values.  
  
 `_CStr`  
 A C-style string of zeros and ones used to initialize the bitset bit values.  
  
 `_Pos`  
 The position of the character in the string, counting from left to right and starting with zero, used to initialize the first bit in the bitset.  
  
 `_Count`  
 The number of characters in the string that is used to provide initial values for the bits in the bitset.  
  
 `_Zero`  
 The character that is used to represent a zero. The default is '0'.  
  
 `_One`  
 The character that is used to represent a one. The default is '1'.  
  
### Remarks  
 Three constructors can be used to construct obects of class                         `bitset<N>`:  
  
-   The first constructor accepts no parameters, constructs an object of class                                 `bitset<N>` and initializes all N bits to a default value of zero.  
  
-   The second constructor constructs an object of class                                 `bitset<N>` and initializes the bits by using the single                                 `unsigned long long` parameter.  
  
-   The third constructor constructs an object of class                                 `bitset<N>`, initializing the N bits to values that correspond to the characters provided in a c-style character string of zeros and ones. You call the constructor without casting the string into a string type:                                 `bitset<5> b5("01011");`  
  
 There are also two constructor templates provided:  
  
-   The first constructor template constructs an object of class                                 `bitset<N>` and initializes bits from the characters provided in a string of zeros and ones. If any characters of the string are other than 0 or 1, the constructor throws an object of class                                 [invalid argument](../vs140/invalid_argument-Class.md). If the position specified (                                `_Pos`) is beyond the length of the string, then the constructor throws an object of class                                 [out_of_range](../vs140/out_of_range-Class.md). The constructor sets only those bits at position                                 *j* in the bitset for which the character in the string at position                                 `_PosÂ +Â j` is 1. By default,                                 `_Pos` is 0.  
  
-   The second constructor template is similar to the first, but includes an additional parameter (                                `_Count`) that is used to specify the number of bits to initialize. It also has two optional parameters,                                 `_Zero` and                                 `_One`, which indicate what character in                                 `_Str` is to be interpreted to mean a 0 bit and a 1 bit, respectively.  
  
### Example  
  
```  
// bitset_bitset.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   // Using the default constructor  
   using namespace std;  
   bitset<2> b0;  
   cout << "The set of bits in bitset<2> b0 is: ( "  
        << b0 << " )." << endl;  
  
   // Using the second member function  
   bitset<5> b1 ( 6 );  
   cout << "The set of bits in bitset<5> b1( 6 ) is: ( "  
        << b1 << " )." << endl;  
  
   // The template parameter N can be an expresssion  
   bitset< 2 * sizeof ( int ) > b2;  
   cout << "The set of bits in bitset<2 * sizeof ( int ) > b2 is: ( "  
        << b2 << " )." << endl;  
  
   // The base two representation will be truncated  
   // if its length exceeds the size of the bitset  
   bitset<3> b3 ( 6 );  
   cout << "The set of bits in bitset<3> b3( 6 ) is ( "  
        << b3 << " )." << endl;  
  
   // Using a c-style string to initialize the bitset  
    bitset<7> b3andahalf ( "1001001" );  
    cout << "The set of bits in bitset<7> b3andahalf ( \"1001001\" )"  
         << " is ( " << b3andahalf << " )." << endl;   
  
   // Using the fifth member function with the first parameter  
   string bitval4 ( "10011" );  
   bitset<5> b4 ( bitval4 );  
   cout << "The set of bits in bitset<5> b4( bitval4 ) is ( "  
        << b4 << " )." << endl;  
  
   // Only part of the string may be used for initialization  
  
   // Starting at position 3 for a length of 6 (100110)  
   string bitval5 ("11110011011");  
   bitset<6> b5 ( bitval5, 3, 6 );  
   cout << "The set of bits in bitset<11> b5( bitval, 3, 6 ) is ( "  
        << b5 << " )." << endl;  
  
   // The bits not initialized with part of the string  
   // will default to zero  
   bitset<11> b6 ( bitval5, 3, 5 );  
   cout << "The set of bits in bitset<11> b6( bitval5, 3, 5 ) is ( "  
        << b6 << " )." << endl;  
  
   // Starting at position 2 and continue to the end of the string  
   bitset<9> b7 ( bitval5, 2 );  
   cout << "The set of bits in bitset<9> b7( bitval, 2 ) is ( "  
        << b7 << " )." << endl;  
}  
```  
  
  **The set of bits in bitset<2> b0 is: ( 00 ).**  
**The set of bits in bitset<5> b1( 6 ) is: ( 00110 ).**  
**The set of bits in bitset<2 \* sizeof ( int ) > b2 is: ( 00000000 ).**  
**The set of bits in bitset<3> b3( 6 ) is ( 110 ).**  
**The set of bits in bitset<5> b4( bitval4 ) is ( 10011 ).**  
**The set of bits in bitset<11> b5( bitval, 3, 6 ) is ( 100110 ).**  
**The set of bits in bitset<11> b6( bitval5, 3, 5 ) is ( 00000010011 ).**  
**The set of bits in bitset<9> b7( bitval, 2 ) is ( 110011011 ).**    
##  <a name="bitset__count"></a>  bitset::count  
 Returns the number of bits set in the bit sequence.  
  
```  
  
size_t count( ) const;  
  
```  
  
### Return Value  
 The number of bits set in the bit sequence.  
  
### Example  
  The following example demonstrates the use of the bitset::count member function.  
  
```  
// bitset_count.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
    using namespace std;  
  
    bitset<5> b1(4);  
  
    cout << "The collection of bits in the original bitset is: ( "  
         << b1 << " )" << endl;  
  
    size_t i;  
    i = b1.count();  
    cout << "The number of bits in the bitset set to 1 is: "  
         << i << "." << endl;  
  
    bitset<5> fb1;  
    fb1 = b1.flip();  
  
    cout << "The collection of flipped bits in the modified bitset "  
         << "is: ( " << b1 << " )" << endl;  
  
    size_t ii;  
    ii = fb1.count();  
    cout << "The number of bits in the bitset set to 1 is: "  
         << ii << "." << endl;  
}  
```  
  
  **The collection of bits in the original bitset is: ( 00100 )**  
**The number of bits in the bitset set to 1 is: 1.**  
**The collection of flipped bits in the modified bitset is: ( 11011 )**  
**The number of bits in the bitset set to 1 is: 4.**    
##  <a name="bitset__element_type"></a>  bitset::element_type  
 A type that is a synonym for the data type                 `bool` and can be used to reference element bits in a bitset.  
  
```  
  
typedef bool element_type;  
  
```  
  
### Example  
  
```  
// bitset_elem_type.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<3> b1 ( 2 );  
   cout << "Original bitset b1(6) is: ( "<< b1 << " )"  
        << endl;  
  
   //Compare two ways to reference bits in a bitset  
   bool b;  
   bitset<5>::element_type e;  
  
   b = b1.test ( 2 );  
   if ( b )  
      cout << "The bit at position 2 of bitset b1"  
           << "has a value of 1." << endl;  
   else  
      cout << "The bit at position 2 of bitset b1"  
           << "has a value of 0." << endl;  
   b1[2] = 1;  
   cout << "Bitset b1 modified by b1[2] = 1 is: ( "<< b1 << " )"  
        << endl;  
  
   e = b1.test ( 2 );  
   if ( e )  
      cout << "The bit at position 2 of bitset b1"  
           << "has a value of 1." << endl;  
   else  
      cout << "The bit at position 2 of bitset b1"  
           << "has a value of 0." << endl;  
}  
```  
  
  **Original bitset b1(6) is: ( 010 )**  
**The bit at position 2 of bitset b1has a value of 0.**  
**Bitset b1 modified by b1[2] = 1 is: ( 110 )**  
**The bit at position 2 of bitset b1has a value of 1.**    
##  <a name="bitset__flip"></a>  bitset::flip  
 Toggles the value of all the bits in a bitset or toggles a single bit at a specified position.  
  
```  
  
bitset<N>& flip( );Â   
bitset<N>& flip(  
   size_t   
_Pos  
);  
  
```  
  
### Parameters  
 `_Pos`  
 The position of the bit whose value is to be toggled.  
  
### Return Value  
 A copy of the modified bitset for which the member function was invoked.  
  
### Remarks  
 The second member function throws an                         [out_of_range](../vs140/out_of_range-Class.md) exception if the position specified as a parameter is greater than the size                         *N* of the                         **bitset<***N***>** whose bit was toggled.  
  
### Example  
  
```  
// bitset_flip.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   bitset<5> b1 ( 6 );  
  
   cout << "The collection of bits in the original bitset is: ( "  
        << b1 << " )" << endl;  
  
   bitset<5> fb1;  
   fb1 = b1.flip ( );  
  
   cout << "After flipping all the bits, the bitset becomes: ( "  
        << fb1 << " )" << endl;  
  
   bitset<5> f3b1;  
   f3b1 = b1.flip ( 3 );  
  
   cout << "After flipping the fourth bit, the bitset becomes: ( "  
        << f3b1 << " )" << endl << endl;  
  
   bitset<5> b2;  
   int i;  
   for ( i = 0 ; i <= 4 ; i++ )  
   {  
      b2.flip(i);  
      cout << b2 << "  The bit flipped is in position "  
           << i << ".\n";  
   }  
}  
```  
  
  **The collection of bits in the original bitset is: ( 00110 )**  
**After flipping all the bits, the bitset becomes: ( 11001 )**  
**After flipping the fourth bit, the bitset becomes: ( 10001 )**  
**00001  The bit flipped is in position 0.**  
**00011  The bit flipped is in position 1.**  
**00111  The bit flipped is in position 2.**  
**01111  The bit flipped is in position 3.**  
**11111  The bit flipped is in position 4.**    
##  <a name="bitset__none"></a>  bitset::none  
 Tests if no bit has been set to 1 in a bitset object.  
  
```  
  
bool none( ) const;  
  
```  
  
### Return Value  
 **true** if no bit in the bitset has been set to 1;                         **false** if at least one bit has been set to 1.  
  
### Example  
  
```  
// bitset_none.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 6 );  
   bool b, rb;  
  
   cout << "Original bitset b1(6) is: ( " << b1 << " )"  
        << endl;  
  
   b = b1.none ( );  
  
   if ( b )  
      cout << "None of the bits in bitset b1 are set to 1."  
           << endl;  
   else  
      cout << "At least one of the bits in bitset b1 is set to 1."  
           << endl;  
  
   bitset<5> rb1;  
   rb1 = b1.reset ( );  
   rb = rb1.none ( );  
   if ( rb )  
      cout << "None of the bits in bitset b1 are set to 1."  
           << endl;  
   else  
      cout << "At least one of the bits in bitset b1 is set to 1."  
           << endl;  
}  
```  
  
  **Original bitset b1(6) is: ( 00110 )**  
**At least one of the bits in bitset b1 is set to 1.**  
**None of the bits in bitset b1 are set to 1.**    
##  <a name="bitset__operator_neq"></a>  bitset::operator!=  
 Tests a target bitset for inequality with a specified bitset.  
  
```  
  
bool operator !=(  
   const bitset<N>&   
_Right  
) const;  
  
```  
  
### Parameters  
 `_Right`  
 The bitset that is to be compared to the target bitset for inequality.  
  
### Return Value  
 **true** if the bitsets are different;                         **false** if they are the same.  
  
### Remarks  
 Bitsets must be of the same size to be tested for inequality by the member operator function.  
  
### Example  
  
```  
// bitset_op_NE.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 7 );  
   bitset<5> b2 ( 7 );  
   bitset<5> b3 ( 2 );  
   bitset<4> b4 ( 7 );  
  
   if ( b1 != b2 )  
      cout << "Bitset b1 is different from bitset b2." << endl;  
   else  
      cout << "Bitset b1 is the same as bitset b2." << endl;  
  
   if ( b1 != b3 )  
      cout << "Bitset b1 is different from bitset b3." << endl;  
   else  
      cout << "Bitset b1 is the same as bitset b3." << endl;  
  
   // This would cause an error because bitsets must have the  
   // same size to be tested  
   // if ( b1 != b4 )  
   //   cout << "Bitset b1 is different from bitset b4." << endl;  
   // else  
   //   cout << "Bitset b1 is the same as bitset b4." << endl;  
}  
```  
  
  **Bitset b1 is the same as bitset b2.**  
**Bitset b1 is different from bitset b3.**    
##  <a name="bitset__operator_amp__eq"></a>  bitset::operator&amp;=  
 Performs a bitwise combination of bitsets with the logical                 **AND** operation.  
  
```  
  
bitset<N>& operator&=(  
   const bitset<N>&   
_Right  
);  
  
```  
  
### Parameters  
 `_Right`  
 The bitset that is to be combined bitwise with the target bitset.  
  
### Return Value  
 The modified target bitset that results from the bitwise                         **AND** operation with the bitset specified as a parameter.  
  
### Remarks  
 Two bits combined by the                         **AND** operator return                         **true** if each bit is true; otherwise, their combination returns                         **false**.  
  
 Bitsets must be of the same size to be combined bitwise with the                         **AND** operator by the member operator function.  
  
### Example  
  
```  
// bitset_op_bitwise.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 7 );  
   bitset<5> b2 ( 11 );  
   bitset<4> b3 ( 7 );  
  
   cout << "The target bitset b1 is:    ( "<< b1 << " )." << endl;  
   cout << "The parameter bitset b2 is: ( "<< b2 << " )." << endl;  
   cout << endl;  
  
   b1 &= b2;  
   cout << "After bitwise AND combination,\n"  
        << " the target bitset b1 becomes:   ( "<< b1 << " )."   
        << endl;  
  
   // Note that the parameter-specified bitset is unchanged  
   cout << "The parameter bitset b2 remains: ( "<< b2 << " )."   
        << endl;  
  
   // The following would cause an error because the bisets   
   // must be of the same size to be combined  
   // b1 &= b3;  
}  
```  
  
  **The target bitset b1 is:    ( 00111 ).**  
**The parameter bitset b2 is: ( 01011 ).**  
**After bitwise AND combination,**  
 **the target bitset b1 becomes:   ( 00011 ).**  
**The parameter bitset b2 remains: ( 01011 ).**    
##  <a name="bitset__operator_lt__lt_"></a>  bitset::operator&lt;&lt;  
 Shifts the bits in a bitset to the left a specified number of positions and returns the result to a new bitset.  
  
```  
bitset<N> operator<<(  
   size_t                 _Pos  
) const;  
```  
  
### Parameters  
 `_Pos`  
 The number of positions to the left that the bits in the bitset are to be shifted.  
  
### Return Value  
 The modified bitset with the bits shifted to the left the required number of positions.  
  
### Remarks  
 The member operator function returns                         **bitset**(                        **\*this**)                         **<<= pos,** where                         [<<=](#bitset__operator_lt__lt__eq) shifts the bits in a bitset to the left a specified number of positions and returns the result to the targeted bitset.  
  
### Example  
  
```  
// bitset_op_LS.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 7 );  
  
   cout << "The bitset b1 is: ( "<< b1 << " )." << endl;  
  
   bitset<5> b2;  
   b2 = b1 << 2;  
  
   cout << "After shifting the bits 2 positions to the left,\n"  
        << " the bitset b2 is: ( "<< b2 << " )."  
        << endl;  
  
   bitset<5> b3 = b2 >> 1;  
  
   cout << "After shifting the bits 1 position to the right,\n"  
        << " the bitset b3 is: ( " << b3 << " )."  
        << endl;  
}  
```  
  
##  <a name="bitset__operator_lt__lt__eq"></a>  bitset::operator&lt;&lt;=  
 Shifts the bits in a bitset to the left a specified number of positions and returns the result to the targeted bitset.  
  
```  
bitset<N>& operator<<=(  
   size_t                 _Pos  
);  
```  
  
### Parameters  
 `_Pos`  
 The number of positions to the left the bits in the bitset are to be shifted.  
  
### Return Value  
 The targeted bitset modified so that the bits have been shifted to the left the required number of positions.  
  
### Remarks  
 If no element exists to shift into the position, the function clears the bit to a value of 0.  
  
### Example  
  
```  
// bitset_op_LSE.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   bitset<5> b1 ( 7 );  
   cout << "The target bitset b1 is: ( "<< b1 << " )." << endl;  
   b1 <<= 2;  
   cout << "After shifting the bits 2 positions to the left,\n"  
        << " the target bitset b1 becomes: ( "<< b1 << " )."   
        << endl;  
}  
```  
  
  **The target bitset b1 is: ( 00111 ).**  
**After shifting the bits 2 positions to the left,**  
 **the target bitset b1 becomes: ( 11100 ).**    
##  <a name="bitset__operator_eq_eq"></a>  bitset::operator==  
 Tests a target bitset for equality with a specified bitset.  
  
```  
  
bool operator ==(  
   const bitset<N>&   
_Right  
) const;  
  
```  
  
### Parameters  
 `_Right`  
 The bitset that is to be compared to the target bitset for equality.  
  
### Return Value  
 **true** if the bitsets are the same;                         **false** if they are different.  
  
### Remarks  
 Bitsets must be of the same size to be tested for equality by the member operator function.  
  
### Example  
  
```  
// bitset_op_EQ.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   bitset<5> b1 ( 7 );  
   bitset<5> b2 ( 7 );  
   bitset<5> b3 ( 2 );  
   bitset<4> b4 ( 7 );  
  
   if ( b1 == b2 )  
      cout << "Bitset b1 is the same as bitset b2." << endl;  
   else  
      cout << "Bitset b1 is different from bitset b2." << endl;  
  
   if ( b1 == b3 )  
      cout << "Bitset b1 is the same as bitset b3." << endl;  
   else  
      cout << "Bitset b1 is different from bitset b3." << endl;  
  
   // This would cause an error because bitsets must have the   
   // same size to be tested  
   // if ( b1 == b4 )  
   //   cout << "Bitset b1 is the same as bitset b4." << endl;  
   // else  
   //   cout << "Bitset b1 is different from bitset b4." << endl;  
}  
```  
  
  **Bitset b1 is the same as bitset b2.**  
**Bitset b1 is different from bitset b3.**    
##  <a name="bitset__operator_gt__gt_"></a>  bitset::operator&gt;&gt;  
 Shifts the bits in a bitset to the right a specified number of positions and returns the result to a new bitset.  
  
```  
bitset<N> operator>>(  
   size_t                 _Pos  
) const;  
```  
  
### Parameters  
 `_Pos`  
 The number of positions to the right the bits in the bitset are to be shifted.  
  
### Return Value  
 A new bitset where the bits have been shifted to the right the required number of positions relative to the targeted bitset.  
  
### Example  
  
```  
// bitset_op_RS.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   bitset<5> b1 ( 7 );  
   cout << "The bitset b1 is: ( "<< b1 << " )." << endl;  
  
   bitset<5> b2;  
   b2 = b1 << 2;  
  
   cout << "After shifting the bits 2 positions to the left,\n"  
        << " the bitset b2 is: ( "<< b2 << " )."  
        << endl;  
   bitset<5> b3 = b2 >> 1;  
  
   cout << "After shifting the bits 1 position to the right,\n"  
        << " the bitset b3 is: ( " << b3 << " )."  
        << endl;  
}  
```  
  
  **The bitset b1 is: ( 00111 ).**  
**After shifting the bits 2 positions to the left,**  
 **the bitset b2 is: ( 11100 ).**  
**After shifting the bits 1 position to the right,**  
 **the bitset b3 is: ( 01110 ).**    
##  <a name="bitset__operator_gt__gt__eq"></a>  bitset::operator&gt;&gt;=  
 Shifts the bits in a bitset to the right a specified number of positions and returns the result to the targeted bitset.  
  
```  
bitset<N>& operator>>=(  
   size_t                 _Pos  
);  
```  
  
### Parameters  
 `_Pos`  
 The number of positions to the right the bits in the bitset are to be shifted.  
  
### Return Value  
 The targeted bitset modified so that the bits have been shifted to the right the required number of positions.  
  
### Remarks  
 If no element exists to shift into the position, the function clears the bit to a value of 0.  
  
### Example  
  
```  
// bitset_op_RSE.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   bitset<5> b1 ( 28 );  
   cout << "The target bitset b1 is: ( "<< b1 << " )." << endl;  
  
   b1 >>= 2;  
   cout << "After shifting the bits 2 positions to the right,\n"  
        << " the target bitset b1 becomes: ( "<< b1 << " )."   
        << endl;  
}  
```  
  
  **The target bitset b1 is: ( 11100 ).**  
**After shifting the bits 2 positions to the right,**  
 **the target bitset b1 becomes: ( 00111 ).**    
##  <a name="bitset__operator_at"></a>  bitset::operator[]  
 Returns a reference to a bit at a specified position in a bitset if the bitset is modifiable; otherwise, it returns the value of the bit at that position.  
  
```  
bool operator[](size_t                 _Pos) const;  
reference operator[](size_t                 _Pos);  
```  
  
### Parameters  
 `_Pos`  
 The position locating the bit within the bitset.  
  
### Remarks  
 When compiling with _SECURE_SCL 1, a runtime error will occur if you attempt to access an element outside the bounds of the bitset.  See                         [Checked Iterators](../vs140/Checked-Iterators.md) for more information.  
  
### Example  
  
```  
// bitset_op_REF.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   bool b;  
   bitset<5> b1 ( 6 );  
   cout << "The initialized bitset<5> b1( 2 ) is: ( "<< b1 << " )."  
        << endl;  
  
   int i;  
   for ( i = 0 ; i <= 4 ; i++ )  
   {  
      b = b1[ i ];  
      cout << "  The bit in position "  
           << i << " is " << b << ".\n";  
   }  
}  
```  
  
##  <a name="bitset__operator_xor_eq"></a>  bitset::operator^=  
 Performs a bitwise combination of bitsets with the exclusive                 `OR` operation.  
  
```  
  
bitset<N>& operator^=(  
   const bitset<N>&   
_Right  
);  
  
```  
  
### Parameters  
 `_Right`  
 The bitset that is to be combined bitwise with the target bitset.  
  
### Return Value  
 The modified target bitset that results from the bitwise exclusive                         `OR` operation with the bitset specified as a parameter.  
  
### Remarks  
 Two bits combined by the exclusive                         **OR** operator return                         **true** if at least one, but not both, of the bits is                         **true**; otherwise, their combination returns                         **false**.  
  
 Bitsets must be of the same size to be combined bitwise with the exclusive                         `OR` operator by the member operator function.  
  
### Example  
  
```  
// bitset_op_bitwiseOR.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   bitset<5> b1 ( 7 );  
   bitset<5> b2 ( 11 );  
   bitset<4> b3 ( 7 );  
  
   cout << "The target bitset b1 is:    ( "<< b1 << " )." << endl;  
   cout << "The parameter bitset b2 is: ( "<< b2 << " )." << endl;  
   cout << endl;  
  
   b1 ^= b2;  
   cout << "After bitwise exclusive OR combination,\n"  
        << " the target bitset b1 becomes:   ( "<< b1 << " )."   
        << endl;  
  
   // Note that the parameter-specified bitset in unchanged  
   cout << "The parameter bitset b2 remains: ( "<< b2 << " )."   
        << endl;  
  
   // The following would cause an error because the bisets   
   // must be of the same size to be combined  
   // b1 |= b3;  
}  
```  
  
  **The target bitset b1 is:    ( 00111 ).**  
**The parameter bitset b2 is: ( 01011 ).**  
**After bitwise exclusive OR combination,**  
 **the target bitset b1 becomes:   ( 01100 ).**  
**The parameter bitset b2 remains: ( 01011 ).**    
##  <a name="bitset__operator_or_eq"></a>  bitset::operator&#124;=  
 Performs a bitwise combination of bitsets with the inclusive                 `OR` operation.  
  
```  
  
bitset<N>& operator|=(  
   const bitset<N>&   
_Right  
);  
  
```  
  
### Parameters  
 `_Right`  
 The bitset that is to be combined bitwise with the target bitset.  
  
### Return Value  
 The modified target bitset that results from the bitwise inclusive                         `OR` operation with the bitset specified as a parameter.  
  
### Remarks  
 Two bits combined by the inclusive                         `OR` operator return                         **true** if at least one of the bits is                         **true**; if both bits are                         **false**, their combination returns                         **false**.  
  
 Bitsets must be of the same size to be combined bitwise with the inclusive                         `OR` operator by the member operator function.  
  
### Example  
  
```  
// bitset_op_BIO.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 7 );  
   bitset<5> b2 ( 11 );  
   bitset<4> b3 ( 7 );  
  
   cout << "The target bitset b1 is:    ( "<< b1 << " )." << endl;  
   cout << "The parameter bitset b2 is: ( "<< b2 << " )." << endl;  
   cout << endl;  
  
   b1 |= b2;  
   cout << "After bitwise inclusive OR combination,\n"  
        << " the target bitset b1 becomes:   ( "<< b1 << " )."   
        << endl;  
  
   // Note that the parameter-specified bitset in unchanged  
   cout << "The parameter bitset b2 remains: ( "<< b2 << " )."   
        << endl;  
  
   // The following would cause an error because the bisets   
   // must be of the same size to be combined  
   // b1 |= b3;  
}  
```  
  
  **The target bitset b1 is:    ( 00111 ).**  
**The parameter bitset b2 is: ( 01011 ).**  
**After bitwise inclusive OR combination,**  
 **the target bitset b1 becomes:   ( 01111 ).**  
**The parameter bitset b2 remains: ( 01011 ).**    
##  <a name="bitset__operator_dtor"></a>  bitset::operator~  
 Toggles all the bits in a target bitset and returns the result.  
  
```  
bitset<N> operator~( ) const;  
```  
  
### Return Value  
 The bitset with all its bits toggled with respect to the targeted bitset.  
  
### Example  
  
```  
// bitset_op_toggle.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <string>  
#include <bitset>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 7 );  
   bitset<5> b2;  
   b2 = ~b1;  
  
   cout << "Bitset b1 is: ( "<< b1 << " )." << endl;  
   cout << "Bitset b2 = ~b1 is: ( "<< b2 << " )." << endl;  
  
   // These bits could also be flipped using the flip member function  
   bitset<5> b3;  
   b3 = b1.flip( );  
   cout << "Bitset b3 = b1.flip( ) is: ( "<< b2 << " )." << endl;  
}  
```  
  
  **Bitset b1 is: ( 00111 ).**  
**Bitset b2 = ~b1 is: ( 11000 ).**  
**Bitset b3 = b1.flip( ) is: ( 11000 ).**    
##  <a name="bitset__reference"></a>  bitset::reference  
 A proxy class that provides references to bits contained in a bitset that is used to access and manipulate the individual bits as a helper class for the                 `operator[]` of class bitset.  
  
```  
class reference {  
   friend class bitset<N>;  
   public:  
      reference& operator=(  
         bool                 _Val  
      );  
      reference& operator=(  
         const reference&                 _Bitref  
      );  
      bool operator~( ) const;  
      operator bool( ) const;  
      reference& flip( );  
};  
```  
  
### Parameters  
 `_Val`  
 The value of the object of type                                 `bool` to be assigned to a bit in a bitset.  
  
 `_Bitref`  
 A reference of the form                                 *x [ i ]* to the bit at position                                 *i* in bitset                                 *x*.  
  
### Return Value  
 A reference to the bit in the bitset specified by the argument position for the first, second, and fifth member functions of class reference, and                         **true** or                         **false**, to reflect the value of the modified bit in the bitset for the third and fourth member functions of class reference.  
  
### Remarks  
 The class reference exists only as a helper class for the bitset                         `operator[]`. The member class describes an object that can access an individual bit within a bitset. Let                         *b* be an object of type                         `bool`,                         *x* and                         *y* objects of type                         **bitset<***N***>**, and                         *i* and                         *j* valid positions within such an object. The notation                         *x [i]* references the bit at position                         *i* in bitset                         *x*. The member functions of class reference provide, in order, the following operations:  
  
|Operation|Definition|  
|---------------|----------------|  
|*x*[                                        *i*] =                                         *b*|Stores                                         `bool` value                                         *b* at bit position                                         *i* in bitset                                         *x*.|  
|*x*[                                        *i*] =                                         *y*[                                        *j*]|Stores the value of the bit                                         *y*[                                        *j*] at bit position                                         *i* in bitset                                         *x*.|  
|*b* = ~                                        *x*[                                        *i*]|Stores the flipped value of the bit                                         *x*[                                        *i*] in                                         `bool`Â                                         *b*.|  
|*b* =                                         *x*[                                        *i*]|Stores the value of the bit                                         *x*[                                        *i*] in                                         `bool`Â                                         *b*.|  
|*x*[                                        *i*].                                        `flip`( )|Stores the flipped value of the bit                                         *x*[                                        *i*] back at bit position                                         *i* in                                         *x*.|  
  
### Example  
  
```  
// bitset_reference.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 2 );  
   bitset<5> b2 ( 6 );  
   cout << "The initialized bitset<5> b1( 2 ) is: ( "<< b1 << " )."  
        << endl;  
   cout << "The initialized bitset<5> b2( 6 ) is: ( "<< b2 << " )."  
        << endl;  
  
   // Example of x [i] = b storing bool b at bit position i  
   // in bitset x  
   b1[ 0 ] = true;  
   cout << "The bitset<5> b1 with the bit at position 0 set to 1"  
        << " is: ( "<< b1 << " )" << endl;  
  
   // Example of x [i] = y [j] storing the bool value of the  
   // bit at position j in bitset y at bit position i in bitset x  
   b2 [4] = b1 [0];      // b1 [0] = true  
   cout << "The bitset<5> b2 with the bit at position 4 set to the "  
        << "value\n of the bit at position 0 of the bit in "  
        << "bitset<5> b1 is: ( "<<  b2  << " )" << endl;  
  
   // Example of b = ~x [i] flipping the value of the bit at  
   // position i of bitset x and storing the value in an   
   // object b of type bool  
   bool b = ~b2 [4];      // b2 [4] = false  
   if ( b )  
      cout << "The value of the object b = ~b2 [4] "  
           << "of type bool is true." << endl;  
   else  
      cout << "The value of the object b = ~b2 [4] "  
           << "of type bool is false." << endl;  
  
   // Example of b = x [i] storing the value of the bit at  
   // position i of bitset x in the object b of type bool  
   b = b2 [4];  
   if ( b )  
      cout << "The value of the object b = b2 [4] "  
           << "of type bool is true." << endl;  
   else  
      cout << "The value of the object b = b2 [4] "  
           << "of type bool is false." << endl;  
  
   // Example of x [i] . flip ( ) toggling the value of the bit at  
   // position i of bitset x  
   cout << "Before flipping the value of the bit at position 4 in "  
        << "bitset b2,\n it is ( "<<  b2  << " )." << endl;  
   b2 [4].flip( );  
   cout << "After flipping the value of the bit at position 4 in "  
        << "bitset b2,\n it becomes ( "<<  b2  << " )." << endl;  
   bool c;  
   c = b2 [4].flip( );  
   cout << "After a second toggle, the value of the position 4"  
        << " bit in b2 is now: " << c << ".";  
}  
```  
  
  **The initialized bitset<5> b1( 2 ) is: ( 00010 ).**  
**The initialized bitset<5> b2( 6 ) is: ( 00110 ).**  
**The bitset<5> b1 with the bit at position 0 set to 1 is: ( 00011 )**  
**The bitset<5> b2 with the bit at position 4 set to the value**  
 **of the bit at position 0 of the bit in bitset<5> b1 is: ( 10110 )**  
**The value of the object b = ~b2 [4] of type bool is false.**  
**The value of the object b = b2 [4] of type bool is true.**  
**Before flipping the value of the bit at position 4 in bitset b2,**  
 **it is ( 10110 ).**  
**After flipping the value of the bit at position 4 in bitset b2,**  
 **it becomes ( 00110 ).**  
**After a second toggle, the value of the position 4 bit in b2 is now: 1.**    
##  <a name="bitset__reset"></a>  bitset::reset  
 Resets all the bits in a bitset to 0 or resets a bit at a specified position to 0.  
  
```  
  
bitset<N>& reset( );Â   
bitset<N>& reset(  
   size_t   
_Pos  
);  
  
```  
  
### Parameters  
 `_Pos`  
 The position of the bit in the bitset to be reset to 0.  
  
### Return Value  
 A copy of the bitset for which the member function was invoked.  
  
### Remarks  
 The second member function throws an                         [out_of_range](../vs140/out_of_range-Class.md) exception if the position specified is greater than the size of the bitset.  
  
### Example  
  
```  
// bitset_reset.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 13 );  
   cout << "The set of bits in bitset<5> b1(13) is: ( "<< b1 << " )"  
        << endl;  
  
   bitset<5> b1r3;  
   b1r3 = b1.reset( 2 );  
   cout << "The collecion of bits obtained from resetting the\n"  
        << " third bit of bitset b1 is: ( "<< b1r3 << " )"   
        << endl;  
  
   bitset<5> b1r;  
   b1r = b1.reset( );  
   cout << "The collecion of bits obtained from resetting all\n"  
        << " the elements of the bitset b1 is: ( "<< b1r << " )"  
        << endl;  
}  
```  
  
  **The set of bits in bitset<5> b1(13) is: ( 01101 )**  
**The collecion of bits obtained from resetting the**  
 **third bit of bitset b1 is: ( 01001 )**  
**The collecion of bits obtained from resetting all**  
 **the elements of the bitset b1 is: ( 00000 )**    
##  <a name="bitset__set"></a>  bitset::set  
 Sets all the bits in a bitset to 1 or sets a bit at a specified position to 1.  
  
```  
  
bitset<N>& set( );  
bitset<N>& set(  
   size_t   
_Pos  
,   
   bool   
_Val  
 = true  
);  
  
```  
  
### Parameters  
 `_Pos`  
 The position of the bit in the bitset to be set to assigned a value.  
  
 `_Val`  
 The value to be assigned to the bit at the position specified.  
  
### Return Value  
 A copy of the bitset for which the member function was invoked.  
  
### Remarks  
 The second member function throws an                         [out_of_range](../vs140/out_of_range-Class.md) exception if the position specified is greater than the size of the bitset.  
  
### Example  
  
```  
// bitset_set.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 6 );  
   cout << "The set of bits in bitset<5> b1(6) is: ( "<< b1 << " )"  
        << endl;  
  
   bitset<5> b1s0;  
   b1s0 = b1.set( 0 );  
   cout << "The collecion of bits obtained from setting the\n"  
        << " zeroth bit of bitset b1 is: ( "<< b1s0 << " )"   
        << endl;  
  
   bitset<5> bs1;  
   bs1 = b1.set( );  
   cout << "The collecion of bits obtained from setting all the\n"  
        << " elements of the bitset b1 is: ( "<< bs1 << " )"  
        << endl;  
}  
```  
  
  **The set of bits in bitset<5> b1(6) is: ( 00110 )**  
**The collecion of bits obtained from setting the**  
 **zeroth bit of bitset b1 is: ( 00111 )**  
**The collecion of bits obtained from setting all the**  
 **elements of the bitset b1 is: ( 11111 )**    
##  <a name="bitset__size"></a>  bitset::size  
 Returns the number of bits in a bitset object.  
  
```  
  
size_t  
size( ) const;  
  
```  
  
### Return Value  
 The number of bits,                         *N*, in a                         **bitset<***N***>**.  
  
### Example  
  The following example demonstrates the use of the bitset::size member function.  
  
```  
// bitset_size.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main()  
{  
    using namespace std;  
  
    bitset<5> b1(6);  
    size_t i;  
  
    cout << "The set of bits in bitset<5> b1( 6 ) is: ( "<< b1 << " )"  
         << endl;  
  
    i = b1.size();  
  
    cout << "The number of bits in bitset b1 is: " << i << "."  
         << endl;  
}  
```  
  
  **The set of bits in bitset<5> b1( 6 ) is: ( 00110 )**  
**The number of bits in bitset b1 is: 5.**    
##  <a name="bitset__test"></a>  bitset::test  
 Tests whether the bit at a specified position in a bitset is set to 1.  
  
```  
bool test(  
   size_t                 _Pos,  
) const;  
```  
  
### Parameters  
 `_Pos`  
 The position of the bit in the bitset to be tested for its value.  
  
### Return Value  
 **true** if the bit specified by the argument position is set to 1; otherwise,                         **false**.  
  
### Remarks  
 The member function throws an                         [out_of_range](../vs140/out_of_range-Class.md) exception that is the size of the bitset is less than or equal to the position specified in the argument.  
  
### Example  
  
```  
// bitset_test.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 6 );  
   bool b;  
   bitset<5>::element_type e;  
  
   cout << "Original bitset b1(6) is: ( "<< b1 << " )"  
        << endl;  
   cout << "Note: positions in a bitset are numbered\n"  
         << " from the right starting with 0.\n" << endl;  
  
   b = b1.test ( 3 );  
  
   if ( b )  
      cout << "The bit at position 3 of bitset b1 "  
           << "has a value of 1." << endl;  
   else  
      cout << "The bit at position 3 of bitset b1 "  
           << "has a value of 0." << endl;  
  
   b1[3] = 1;  
   cout << "Bitset b1 modified by b1[3] = 1 is: ( "<< b1 << " )"  
        << endl;  
  
   e = b1.test ( 3 );  
   if ( e )  
      cout << "The bit at position 3 of bitset b1 "  
           << "has a value of 1." << endl;  
   else  
      cout << "The bit at position 3 of bitset b1 "  
           << "has a value of 0." << endl;  
}  
```  
  
  **Original bitset b1(6) is: ( 00110 )**  
**Note: positions in a bitset are numbered**  
 **from the right starting with 0.**  
**The bit at position 3 of bitset b1 has a value of 0.**  
**Bitset b1 modified by b1[3] = 1 is: ( 01110 )**  
**The bit at position 3 of bitset b1 has a value of 1.**    
##  <a name="bitset__to_string"></a>  bitset::to_string  
 Converts a bitset object to a string representation.  
  
```  
  
template<class CharType, class Traits, class Alloc>  
   basic_string<CharType, Traits, Alloc> to_string ( ) const;  
  
```  
  
### Return Value  
 A string object of class basic_string, where each bit set in the bitset has a corresponding character of 1, and a character of 0 if the bit is unset.  
  
### Example  
  
```  
// bitset_to_string.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
#include <string>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 7 );  
  
   cout << "The ordered set of bits in the bitset<5> b1( 7 )"  
        << "\n that was generated by the number 7 is: ( "  
        << b1 << " )" << endl;  
  
   string s1;  
   s1 =  b1.template to_string<char,   
   char_traits<char>, allocator<char> >( );  
   cout << "The string returned from the bitset b1"  
        << "\n by the member function to_string( ) is: "  
        << s1 << "." << endl;  
}  
```  
  
  **The ordered set of bits in the bitset<5> b1( 7 )**  
 **that was generated by the number 7 is: ( 00111 )**  
**The string returned from the bitset b1**  
 **by the member function to_string( ) is: 00111.**    
##  <a name="bitset__to_ullong"></a>  bitset::to_ullong  
 Returns an unsigned long long value that contains the same bits set as the contents of the bitset object.  
  
```  
unsigned long long to_ullong() const;  
```  
  
### Parameters  
  
### Remarks  
 Returns the sum of the bit values in the bit sequence as an unsigned long long.  
  
##  <a name="bitset__to_ulong"></a>  bitset::to_ulong  
 Converts a bitset object to the integer that would generate the sequence of bits contained if used to initialize the bitset.  
  
```  
  
unsigned long to_ulong( ) const;  
  
```  
  
### Return Value  
 An integer that would generate the bits in a bitset if used in the initialization of the bitset.  
  
### Remarks  
 Applying the member function would return the integer that has the same sequence of 1 and 0 digits as is found in sequence of bits contained in the bitset.  
  
 The member function throws                         `overflow_error` if any bit in the bit sequence has a bit value that cannot be represented as a value of type                         `unsigned long`*.*  
  
### Example  
  
```  
// bitset_to_ulong.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   bitset<5> b1 ( 7 );  
  
   cout << "The ordered set of bits in the bitset<5> b1( 7 )"  
        << "\n that was generated by the number 7 is: ( "  
        << b1 << " )" << endl;  
  
   unsigned long int i;  
   i = b1.to_ulong( );  
   cout << "The integer returned from the bitset b1,"  
        << "\n by the member function to_long( ), that"  
        << "\n generated the bits as a base two number is: "  
        << i << "." << endl;  
}  
```  
  
  **The ordered set of bits in the bitset<5> b1( 7 )**  
 **that was generated by the number 7 is: ( 00111 )**  
**The integer returned from the bitset b1,**  
 **by the member function to_long( ), that**  
 **generated the bits as a base two number is: 7.**