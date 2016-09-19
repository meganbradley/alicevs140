---
title: "basic_streambuf::snextc"
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
ms.assetid: e78d04f2-1296-4a7b-b7f6-676de87ba289
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::snextc
Reads the current element and returns the following element.  
  
## Syntax  
  
```  
  
int  
_  
type snextc( );  
  
```  
  
## Return Value  
 The next element in the stream.  
  
## Remarks  
 The member function calls [sbumpc](../vs140/basic_streambuf--sbumpc.md) and, if that function returns **traits_type::**[eof](../vs140/char_traits--eof.md), returns **traits_type::eof**. Otherwise, it returns [sgetc](../vs140/basic_streambuf--sgetc.md).  
  
## Example  
  
```  
// basic_streambuf_snextc.cpp  
// compile with: /EHsc  
#include <iostream>  
int main( )   
{  
   using namespace std;  
   int i = 0;  
   i = cin.rdbuf( )->snextc( );  
   // cout << ( int )char_traits<char>::eof << endl;  
   cout << i << endl;  
}  
```  
  
  **`aa` `aa`97**   
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)