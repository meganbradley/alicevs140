---
title: "basic_streambuf::pbackfail"
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
ms.assetid: 2426bda4-619c-4136-a482-b5b313fb742f
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_streambuf::pbackfail
A protected virtual member function that tries to put back an element into the input stream, then make it the current element (pointed to by the next pointer).  
  
## Syntax  
  
```  
  
      virtual int  
      _  
      type pbackfail(  
   int_type _Meta = traits_type::eof( )  
);  
```  
  
#### Parameters  
 `_Meta`  
 The character to insert into the buffer, or **traits_type::**[eof](../vs140/char_traits--eof.md).  
  
## Return Value  
 If the function cannot succeed, it returns **traits_type::eof** or throws an exception. Otherwise, it returns some other value. The default behavior is to return **traits_type::eof**.  
  
## Remarks  
 If _*Meta* compares equal to **traits_type::eof**, the element to push back is effectively the one already in the stream before the current element. Otherwise, that element is replaced by **traits_type::**[to_char_type](../vs140/char_traits--to_char_type.md)(\_*Meta*). The function can put back an element in various ways:  
  
-   If a putback position is available, it can store the element into the putback position and decrement the next pointer for the input buffer.  
  
-   It can make a putback position available by allocating new or additional storage for the input buffer.  
  
-   For a stream buffer with common input and output streams, it can make a putback position available by writing out, to some external destination, some or all of the elements between the beginning and next pointers for the output buffer.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)