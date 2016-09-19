---
title: "basic_iostream Class"
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
ms.assetid: 294b680b-eb49-4066-8db2-6d52dac9d6e3
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_iostream Class
A stream class that can do both input and output.  
  
## Syntax  
  
```  
template <class Elem, class Tr = char_traits< Elem> >  
    class basic_iostream : public basic_istream< Elem, Tr>,  
        public basic_ostream< Elem, Tr>  
{  
public:  
    explicit basic_iostream(basic_streambuf< Elem, Tr> * _Strbuf);  
    virtual ~basic_iostream();  
};  
```  
  
## Remarks  
 The template class describes an object that controls insertions, through its base class [basic_ostream](../vs140/basic_ostream-Class.md)< `Elem`, `Tr`>, and extractions, through its base class [basic_istream](../vs140/basic_istream-Class.md)< `Elem`, `Tr`>. The two objects share a common virtual base class [basic_ios](../vs140/basic_ios-Class.md)< `Elem`, `Tr`>. They also manage a common stream buffer, with elements of type `Elem`, whose character traits are determined by the class `Tr`. The constructor initializes its base classes through `basic_istream`( **strbuf**) and `basic_ostream`( **strbuf**).  
  
### Constructors  
  
|||  
|-|-|  
|[basic_iostream](#basic_iostream__basic_iostream)|Create a `basic_iostream` object.|  
  
### Member Functions  
  
|||  
|-|-|  
|[swap](#basic_iostream__swap)|Exchanges the contents of the provided `basic_iostream` object for the contents of this object.|  
  
### Operators  
  
|||  
|-|-|  
|[operator=](#basic_iostream__operator_eq)|Assigns the value of a specified `basic_iostream` object to this object. This is a move assignment involving an `rvalue` that does not leave a copy behind.|  
  
## Requirements  
 **Header:** <istream\>  
  
 **Namespace:** std  
  
##  <a name="basic_iostream__basic_iostream"></a>  basic_iostream::basic_iostream  
 Create a `basic_iostream` object.  
  
```  
explicit basic_iostream(basic_streambuf<Elem, Tr> * _Strbuf);  
basic_iostream(basic_iostream&& _Right);  
basic_iostream();  
```  
  
### Parameters  
 `_Strbuf`  
 An existing `basic_streambuf` object.  
  
 `_Right`  
 An existing `basic_iostream` object that is used to construct a new `basic_iostream`.  
  
### Remarks  
 The first constructor initializes the base objects by way of `basic_istream(``_Strbuf``)` and `basic_ostream(``_Strbuf``)`.  
  
 The second constructor initializes the base objects by calling move `(``_Right``)`.  
  
##  <a name="basic_iostream__operator_eq"></a>  basic_iostream::operator=  
 Assign the value of a specified `basic_iostream` object to this object. This is a move assignment involving an `rvalue` that does not leave a copy behind.  
  
```  
basic_iostream& operator=(basic_iostream&& _Right);  
```  
  
### Parameters  
 `_Right`  
 An `rvalue` reference to a `basic_iostream` object to assign from.  
  
### Remarks  
 The member operator calls swap `(``_Right``)`.  
  
##  <a name="basic_iostream__swap"></a>  basic_iostream::swap  
 Exchanges the contents of the provided `basic_iostream` object for the contents of this object.  
  
```  
void swap(basic_iostream& _Right);  
```  
  
### Parameters  
 `_Right`  
 The `basic_iostream` object to swap.  
  
### Remarks  
 The member function calls swap `(``_Right``)`  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)