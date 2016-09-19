---
title: "streampos"
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
ms.assetid: af527446-1ee7-4613-82b6-3ff793c4802e
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# streampos
Holds the current position of the buffer pointer or file pointer.  
  
## Syntax  
  
```  
  
typedef fpos<mbstate  
_  
t> streampos;  
  
```  
  
## Remarks  
 The type is a synonym for [fpos](../vs140/fpos-Class.md)<`mbstate_t`>.  
  
## Example  
  
```  
// ios_streampos.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
  
   ofstream x( "iostream.txt" );  
   x << "testing";  
   streampos y = x.tellp( );  
   cout << y << endl;  
}  
```  
  
 **7**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [fpos Class](../vs140/fpos-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)