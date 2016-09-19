---
title: "ostreambuf_iterator Class"
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
ms.assetid: dad1e624-2f45-4e94-8887-a885e95f9071
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostreambuf_iterator Class
The template class ostreambuf_iterator describes an output iterator object that writes successive character elements onto the output stream with the extraction **operator>>**. The `ostreambuf_iterator`s differ from those of the [ostream_iterator Class](../vs140/ostream_iterator-Class.md) in having characters instead of a generic type at the type of object being inserted into the output stream.  
  
## Syntax  
  
```  
template < class  CharType =  char    class  Traits =  char_traits <CharType> >  
  
```  
  
#### Parameters  
 `CharType`  
 The type that represents the character type for the ostreambuf_iterator. This argument is optional and the default value is `char`*.*  
  
 `Traits`  
 The type that represents the character type for the ostreambuf_iterator. This argument is optional and the default value is `char_traits`<                        *CharType>.*  
  
## Remarks  
 The ostreambuf_iterator class must satisfy the requirements for an output iterator. Algorithms can be written directly to output streams using an `ostreambuf_iterator`. The class provides a low-level stream iterator that allows access to the raw (unformatted) I/O stream in the form of characters and the ability to bypass the buffering and character translations associated with the high-level stream iterators.  
  
### Constructors  
  
|||  
|-|-|  
|[ostreambuf_iterator](#ostreambuf_iterator__ostreambuf_iterator)|Constructs an `ostreambuf_iterator` that is initialized to write characters to the output stream.|  
  
### Typedefs  
  
|||  
|-|-|  
|[char_type](#ostreambuf_iterator__char_type)|A type that provides for the character type of the `ostreambuf_iterator`.|  
|[ostream_type](#ostreambuf_iterator__ostream_type)|A type that provides for the stream type of the `ostream_iterator`.|  
|[streambuf_type](#ostreambuf_iterator__streambuf_type)|A type that provides for the stream type of the `ostreambuf_iterator`.|  
|[traits_type](#ostreambuf_iterator__traits_type)|A type that provides for the character traits type of the `ostream_iterator`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[failed](#ostreambuf_iterator__failed)|Tests for failure of an insertion into the output stream buffer.|  
  
### Operators  
  
|||  
|-|-|  
|[operator*](#ostreambuf_iterator__operator_star)|Dereferencing operator used to implement the output iterator expression * `i` = `x`.|  
|[operator++](#ostreambuf_iterator__operator_add_add)|A nonfunctional increment operator that returns an `ostreambuf_iterator` to the same object it addressed before the operation was called.|  
|[operator=](#ostreambuf_iterator__operator_eq)|The operator inserts a character into the associated stream buffer.|  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
##  <a name="ostreambuf_iterator__char_type"></a>  ostreambuf_iterator::char_type  
 A type that provides for the character type of the `ostreambuf_iterator`.  
  
```  
typedef CharType char_type;  
  
```  
  
### Remarks  
 The type is a synonym for the template parameter **CharType**.  
  
### Example  
  
```  
// ostreambuf_iterator_char_type.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   typedef ostreambuf_iterator<char>::char_type CHT1;  
   typedef ostreambuf_iterator<char>::traits_type CHTR1;  
  
   // ostreambuf_iterator for stream cout  
   // with new line delimiter:  
    ostreambuf_iterator< CHT1, CHTR1> charOutBuf ( cout );  
  
   // Standard iterator interface for writing  
   // elements to the output streambuf:  
   cout << "The characters written to the output stream\n"  
        << " by charOutBuf are: ";  
   *charOutBuf = 'O';  
   charOutBuf++;  
   *charOutBuf = 'U';  
   charOutBuf++;  
   *charOutBuf = 'T';  
   charOutBuf++;  
   cout << "." << endl;  
}  
\* Output:   
The characters written to the output stream  
 by charOutBuf are: OUT.  
*\  
```  
  
##  <a name="ostreambuf_iterator__failed"></a>  ostreambuf_iterator::failed  
 Tests for failure of an insertion into the output stream buffer.  
  
```  
bool failed( ) const throw( );  
  
```  
  
### Return Value  
 **true** if no insertion into the output stream buffer has failed earlier; otherwise **false**.  
  
### Remarks  
 The member function returns **true** if, in any prior use of member `operator=`, the call to **subf**_-> `sputc` returned **eof**.  
  
### Example  
  
```  
// ostreambuf_iterator_failed.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   // ostreambuf_iterator for stream cout  
   ostreambuf_iterator<char> charOut ( cout );  
  
   *charOut = 'a';  
   charOut ++;  
   *charOut  = 'b';  
   charOut ++;     
   *charOut = 'c';  
   cout << " are characters output individually." << endl;  
  
   bool b1 = charOut.failed ( );  
   if (b1)   
       cout << "At least one insertion failed." << endl;  
   else  
       cout << "No insertions failed." << endl;  
}  
\* Output:   
abc are characters output individually.  
No insertions failed.  
*\  
```  
  
##  <a name="ostreambuf_iterator__operator_star"></a>  ostreambuf_iterator::operator*  
 A nonfunctional dereferencing operator used to implement the output iterator expression \*                *i* =                 *x*.  
  
```  
ostreambuf_iterator<CharType, Traits>& operator*( );  
```  
  
### Return Value  
 The ostreambuf iterator object.  
  
### Remarks  
 This operator functions only in the output iterator expression \*                        *i* =                         *x* to output characters to stream buffer. Applied to an ostreambuf iterator, it returns the iterator; **\*iter** returns **iter**,  
  
### Example  
  
```  
// ostreambuf_iterator_op_deref.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   // ostreambuf_iterator for stream cout  
   // with new line delimiter  
   ostreambuf_iterator<char> charOutBuf ( cout );  
  
   // Standard iterator interface for writing  
   // elements to the output stream  
   cout << "Elements written to output stream:" << endl;  
   *charOutBuf = 'O';  
   charOutBuf++;   // no effect on iterator position  
   *charOutBuf = 'U';  
   *charOutBuf = 'T';  
}  
\* Output:   
Elements written to output stream:  
OUT  
*\  
```  
  
##  <a name="ostreambuf_iterator__operator_add_add"></a>  ostreambuf_iterator::operator++  
 A nonfunctional increment operator that returns an ostream iterator to the same character it addressed before the operation was called.  
  
```  
ostreambuf_iterator<CharType, Traits>& operator++( );  
ostreambuf_iterator<CharType, Traits>& operator++( int );  
```  
  
### Return Value  
 A reference to the character originally addressed or to an implementation-defined object that is convertible to `ostreambuf_iterator`< **CharType**, **Traits**>.  
  
### Remarks  
 The operator is used to implement the output iterator expression \*                        *i* =                         *x*.  
  
### Example  
  
```  
// ostreambuf_iterator_op_incr.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   // ostreambuf_iterator for stream cout  
   // with new line delimiter  
   ostreambuf_iterator<char> charOutBuf ( cout );  
  
   // Standard iterator interface for writing  
   // elements to the output stream  
   cout << "Elements written to output stream:" << endl;  
   *charOutBuf = 'O';  
   charOutBuf++;      // No effect on iterator position  
   *charOutBuf = 'U';  
   *charOutBuf = 'T';     
}  
\* Output:   
Elements written to output stream:  
OUT  
*\  
```  
  
##  <a name="ostreambuf_iterator__operator_eq"></a>  ostreambuf_iterator::operator=  
 The operator inserts a character into the associated stream buffer.  
  
```  
ostreambuf_iterator<CharType, Traits>& operator=(  
   CharType _Char  
);  
```  
  
### Parameters  
 `_Char`  
 The character to be inserted into the stream buffer.  
  
### Return Value  
 A reference to the character inserted into the stream buffer.  
  
### Remarks  
 Assignment operator used to implement the output iterator expression \*                        *i* =                         *x* for writing to an output stream.  
  
### Example  
  
```  
// ostreambuf_iterator_op_assign.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   // ostreambuf_iterator for stream cout  
   // with new line delimiter  
   ostreambuf_iterator<char> charOutBuf ( cout );  
  
   // Standard iterator interface for writing  
   // elements to the output stream  
   cout << "Elements written to output stream:" << endl;  
   *charOutBuf = 'O';  
   charOutBuf++;      // No effect on iterator position  
   *charOutBuf = 'U';  
   *charOutBuf = 'T';     
}  
\* Output:   
Elements written to output stream:  
OUT  
*\  
```  
  
##  <a name="ostreambuf_iterator__ostreambuf_iterator"></a>  ostreambuf_iterator::ostreambuf_iterator  
 Constructs an `ostreambuf_iterator` that is initialized to write characters to the output stream.  
  
```  
ostreambuf_iterator(    streambuf_type* _Strbuf ) throw( ); ostreambuf_iterator(    ostream_type& _Ostr ) throw( );  
  
```  
  
### Parameters  
 `_Strbuf`  
 The output streambuf object used to initialize the output stream-buffer pointer.  
  
 `_Ostr`  
 The output stream object used to initialize the output stream-buffer pointer.  
  
### Remarks  
 The first constructor initializes the output stream-buffer pointer with `_Strbuf`.  
  
 The second constructor initializes the output stream-buffer pointer with `_Ostr`. `rdbuf`. The stored pointer must not be a null pointer.  
  
### Example  
  
```  
// ostreambuf_iterator_ostreambuf_iterator.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   // ostreambuf_iterator for stream cout  
   ostreambuf_iterator<char> charOut ( cout );  
  
   *charOut = 'O';  
   charOut ++;  
   *charOut  = 'U';  
   charOut ++;     
   *charOut = 'T';  
   cout << " are characters output individually." << endl;  
  
   ostreambuf_iterator<char> strOut ( cout );  
   string str = "These characters are being written to the output stream.\n ";  
   copy ( str.begin ( ), str. end ( ), strOut );  
}  
\* Output:   
OUT are characters output individually.  
These characters are being written to the output stream.  
*\  
```  
  
##  <a name="ostreambuf_iterator__ostream_type"></a>  ostreambuf_iterator::ostream_type  
 A type that provides for the stream type of the `ostream_iterator`.  
  
```  
typedef basic_ostream<CharType, Traits> ostream_type;  
  
```  
  
### Remarks  
 The type is a synonym for `basic_ostream`< **CharType**, **Traits**>  
  
### Example  
  See [ostreambuf_iterator](#ostreambuf_iterator__ostreambuf_iterator) for an example of how to declare and use `ostream_type`.  
  
##  <a name="ostreambuf_iterator__streambuf_type"></a>  ostreambuf_iterator::streambuf_type  
 A type that provides for the stream type of the `ostreambuf_iterator`.  
  
```  
typedef basic_streambuf<CharType, Traits> streambuf_type;  
  
```  
  
### Remarks  
 The type is a synonym for `basic_streambuf`< **CharType**, **Traits**>, a stream class for I/O buffers that becomes `streambuf` when specialized to character type `char`.  
  
### Example  
  See [ostreambuf_iterator](#ostreambuf_iterator__ostreambuf_iterator) for an example of how to declare and use `streambuf_type`.  
  
##  <a name="ostreambuf_iterator__traits_type"></a>  ostreambuf_iterator::traits_type  
 A type that provides for the character traits type of the `ostream_iterator`.  
  
```  
typedef Traits traits_type;  
  
```  
  
### Remarks  
 The type is a synonym for the template parameter **Traits**.  
  
### Example  
  
```  
// ostreambuf_iterator_traits_type.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   typedef ostreambuf_iterator<char>::char_type CHT1;  
   typedef ostreambuf_iterator<char>::traits_type CHTR1;  
  
   // ostreambuf_iterator for stream cout  
   // with new line delimiter:  
    ostreambuf_iterator< CHT1, CHTR1> charOutBuf ( cout );  
  
   // Standard iterator interface for writing  
   // elements to the output streambuf:  
   cout << "The characters written to the output stream\n"  
        << " by charOutBuf are: ";  
   *charOutBuf = 'O';  
   charOutBuf++;  
   *charOutBuf = 'U';  
   charOutBuf++;  
   *charOutBuf = 'T';  
   charOutBuf++;  
   cout << "." << endl;  
}  
\* Output:   
The characters written to the output stream  
 by charOutBuf are: OUT.  
*\  
```  
  
## See Also  
 [<iterator\>](../vs140/-iterator-.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)