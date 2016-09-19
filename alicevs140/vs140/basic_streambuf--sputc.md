---
title: "basic_streambuf::sputc"
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
ms.assetid: f134b0d5-f8eb-4838-8094-e5628eb603f4
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::sputc
Puts a character into the stream.  
  
## Syntax  
  
```  
  
      int  
      _  
      type sputc(  
   char_type _Ch  
);  
```  
  
#### Parameters  
 `_Ch`  
 The character.  
  
## Return Value  
 Returns the character, if successful.  
  
## Remarks  
 If a `write position` is available, the member function stores `_Ch` in the write position, increments the next pointer for the output buffer, and returns **traits_type::**[to_int_type](../vs140/char_traits--to_int_type.md)(`_Ch`). Otherwise, it returns [overflow](../vs140/basic_streambuf--overflow.md)(`_Ch`).  
  
## Example  
  
```  
// basic_streambuf_sputc.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
  
   int i = cout.rdbuf( )->sputc( 'a' );  
   cout << endl << ( char )i << endl;  
}  
```  
  
 **a**  
**a**   
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)