---
title: "basic_ofstream Class"
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
ms.assetid: 3bcc9c51-6dfc-4844-8fcc-22ef57c9dff1
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ofstream Class
Describes an object that controls insertion of elements and encoded objects into a stream buffer of class [basic_filebuf](../vs140/basic_filebuf-Class.md)< `Elem`, `Tr`>, with elements of type `Elem`, whose character traits are determined by the class `Tr`.  
  
## Syntax  
  
```  
template <class Elem, class Tr = char_traits< Elem> >  
    class basic_ofstream : public basic_ostream< Elem, Tr>  
```  
  
#### Parameters  
 `Elem`  
 The basic element of the file buffer.  
  
 `Tr`  
 The traits of the basic element of the file buffer (usually `char_traits`< `Elem`>).  
  
## Remarks  
 When the `wchar_t` specialization of `basic_ofstream` writes to the file, if the file is opened in text mode it will write a MBCS sequence. The internal representation will use a buffer of `wchar_t` characters.  
  
 The object stores an object of class `basic_filebuf`< `Elem`, `Tr`>.  
  
## Example  
 The following example shows how to create a `basic_ofstream` object and write text to it.  
  
```  
// basic_ofstream_class.cpp  
// compile with: /EHsc  
#include <fstream>  
  
using namespace std;  
  
int main(int argc, char **argv)  
{  
    ofstream ofs("ofstream.txt");  
    if (!ofs.bad())  
    {  
        ofs << "Writing to a basic_ofstream object..." << endl;  
        ofs.close();  
    }  
}  
```  
  
### Constructors  
  
|||  
|-|-|  
|[basic_ofstream](#basic_ofstream__basic_ofstream)|Creates an object of type `basic_ofstream`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[close](#basic_ofstream__close)|Closes a file.|  
|[is_open](#basic_ofstream__is_open)|Determines if a file is open.|  
|[open](#basic_ofstream__open)|Opens a file.|  
|[rdbuf](#basic_ofstream__rdbuf)|Returns the address of the stored stream buffer.|  
|[swap](#basic_ofstream__swap)|Exchange the contents of this `basic_ofstream` for the contents of the provided `basic_ofstream`.|  
  
### Operators  
  
|||  
|-|-|  
|[operator=](#basic_ofstream__operator_eq)|Assigns the content of this stream object. This is a move assignment involving an `rvalue reference` that does not leave a copy behind.|  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
##  <a name="basic_ofstream__basic_ofstream"></a>  basic_ofstream::basic_ofstream  
 Creates an object of type `basic_ofstream`.  
  
```  
basic_ofstream( );  
explicit basic_ofstream(  
    const char * _Filename,  
    ios_base::openmode _Mode = ios_base::out,  
    int _Prot = (int)ios_base::_Openprot  
);  
explicit basic_ofstream(  
    const wchar_t * _Filename,  
    ios_base::openmode _Mode = ios_base::out,  
    int _Prot = (int)ios_base::_Openprot  
);  
basic_ofstream(  
    basic_ofstream&& _Right  
);  
```  
  
### Parameters  
 `_Filename`  
 The name of the file to open.  
  
 `_Mode`  
 One of the enumerations in [ios_base::openmode](../vs140/ios_base-Class.md#ios_base__openmode).  
  
 `_Prot`  
 The default file opening protection, equivalent to the `shflag` parameter in [_fsopen, _wsfopen](../Topic/_fsopen,%20_wfsopen.md).  
  
 `_Right`  
 The rvalue reference to the `basic_ofstream` object being used to initialize this `basic_ofstream` object.  
  
### Remarks  
 The first constructor initializes the base class by calling [basic_ostream](../vs140/basic_ostream-Class.md)( **sb**), where **sb** is the stored object of class [basic_filebuf](../vs140/basic_filebuf-Class.md)< `Elem`, `Tr`>. It also initializes **sb** by calling `basic_filebuf`< `Elem`, `Tr`>.  
  
 The second and third constructors initializes the base class by calling `basic_ostream`( **sb**). It also initializes **sb** by calling `basic_filebuf`< `Elem`, `Tr`> and then **sb**. [open](../vs140/basic_filebuf-Class.md#basic_filebuf__open)( `_Filename`, `_Mode` &#124; `ios_base::out`). If the latter function returns a null pointer, the constructor calls [setstate](../vs140/basic_ios-Class.md#basic_ios__setstate)( **failbit**).  
  
 The fourth constructor is a copy function. It initializes the object with the contents of `right`, treated as an rvalue reference.  
  
### Example  
  The following example shows how to create a `basic_ofstream` object and write text to it.  
  
```  
// basic_ofstream_ctor.cpp  
// compile with: /EHsc  
#include <fstream>  
  
using namespace std;  
  
int main(int argc, char **argv)  
{  
    ofstream ofs("C:\\ofstream.txt");  
    if (!ofs.bad())  
    {  
        ofs << "Writing to a basic_ofstream object..." << endl;  
        ofs.close();  
    }  
}  
```  
  
##  <a name="basic_ofstream__close"></a>  basic_ofstream::close  
 Closes a file.  
  
```  
void close( );  
  
```  
  
### Remarks  
 The member function calls [rdbuf](../vs140/basic_ifstream-Class.md#basic_ifstream__rdbuf)**->**[close](../vs140/basic_filebuf-Class.md#basic_filebuf__close).  
  
### Example  
  See [basic_filebuf::close](../vs140/basic_filebuf-Class.md#basic_filebuf__close) for an example that uses **close**.  
  
##  <a name="basic_ofstream__is_open"></a>  basic_ofstream::is_open  
 Indicates whether a file is open.  
  
```  
bool is_open( ) const;  
```  
  
### Return Value  
 `true` if the file is open, `false` otherwise.  
  
### Remarks  
 The member function returns [rdbuf](#basic_ofstream__rdbuf) **->** [is_open](../vs140/basic_filebuf-Class.md#basic_filebuf__is_open).  
  
### Example  
  
```  
// basic_ofstream_is_open.cpp  
// compile with: /EHsc  
#include <fstream>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   ifstream file;  
   // Open and close with a basic_filebuf  
   file.rdbuf( )->open( "basic_ofstream_is_open.txt", ios::in );  
   file.close( );  
   if (file.is_open())  
      cout << "it's open" << endl;  
   else  
      cout << "it's closed" << endl;  
}  
```  
  
##  <a name="basic_ofstream__open"></a>  basic_ofstream::open  
 Opens a file.  
  
```  
void open(  
    const char * _Filename,  
    ios_base::openmode _Mode = ios_base::out,  
    int _Prot = (int)ios_base::_Openprot  
);  
void open(  
    const char * _Filename,  
    ios_base::openmode _Mode  
);  
void open(  
    const wchar_t * _Filename,  
    ios_base::openmode _Mode = ios_base::out,  
    int _Prot = (int)ios_base::_Openprot  
);  
void open(  
    const wchar_t * _Filename,  
    ios_base::openmode _Mode  
);  
```  
  
### Parameters  
 `_Filename`  
 The name of the file to open.  
  
 `_Mode`  
 One of the enumerations in [ios_base::openmode](../vs140/ios_base-Class.md#ios_base__openmode).  
  
 `_Prot`  
 The default file opening protection, equivalent to the `shflag` parameter in [_fsopen, _wsfopen](../Topic/_fsopen,%20_wfsopen.md).  
  
### Remarks  
 The member function calls [rdbuf](#basic_ofstream__rdbuf) **->** [open](../vs140/basic_filebuf-Class.md#basic_filebuf__open)(_                        *Filename*, `_Mode` &#124; `ios_base::out`). If that function returns a null pointer, the function calls [setstate](../vs140/basic_ios-Class.md#basic_ios__setstate)( **failbit**).  
  
### Example  
  See [basic_filebuf::open](../vs140/basic_filebuf-Class.md#basic_filebuf__open) for an example that uses **open**.  
  
##  <a name="basic_ofstream__operator_eq"></a>  basic_ofstream::operator=  
 Assigns the content of this stream object. This is a move assignment involving an `rvalue reference` that does not leave a copy behind.  
  
```  
basic_ofstream& operator=(  
    basic_ofstream&& _Right  
);  
```  
  
### Parameters  
 `_Right`  
 An rvalue reference to a `basic_ofstream` object.  
  
### Return Value  
 Returns `*this`.  
  
### Remarks  
 The member operator replaces the contents of the object by using the contents of `_Right`, treated as an rvalue reference.  
  
##  <a name="basic_ofstream__rdbuf"></a>  basic_ofstream::rdbuf  
 Returns the address of the stored stream buffer.  
  
```  
basic _ filebuf<Elem, Tr> *rdbuf( ) const  
  
```  
  
### Return Value  
 Returns the address of the stored stream buffer.  
  
### Example  
  See [basic_filebuf::close](../vs140/basic_filebuf-Class.md#basic_filebuf__close) for an example that uses `rdbuf`.  
  
##  <a name="basic_ofstream__swap"></a>  basic_ofstream::swap  
 Exchanges the contents of two `basic_ofstream` objects.  
  
```  
void swap(  
    basic_ofstream& _Right  
);  
```  
  
### Parameters  
 `_Right`  
 An `lvalue` reference to another `basic_ofstream` object.  
  
### Remarks  
 The member function exchanges the contents of this object for the contents of `_Right`.  
  
## See Also  
 [basic_ostream Class](../vs140/basic_ostream-Class.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)