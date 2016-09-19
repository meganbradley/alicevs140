---
title: "wstreampos"
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
ms.assetid: 1444744f-5beb-40c4-9797-675849ab9497
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# wstreampos
Holds the current position of the buffer pointer or file pointer.  
  
## Syntax  
  
```  
  
typedef fpos<mbstate  
_  
t> wstreampos;  
  
```  
  
## Remarks  
 The type is a synonym for [fpos](../vs140/fpos-Class.md)<`mbstate_t`>.  
  
## Example  
  
```  
// ios_wstreampos.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
   wofstream xw( "wiostream.txt" );  
   xw << L"testing";  
   wstreampos y = xw.tellp( );  
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