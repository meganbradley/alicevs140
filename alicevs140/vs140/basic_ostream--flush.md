---
title: "basic_ostream::flush"
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
ms.assetid: 52dd7924-0dbe-486e-8cf3-ebcf887ac9aa
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ostream::flush
Flushes the buffer.  
  
## Syntax  
  
```  
basic_ostream<_Elem, _Tr>& flush( );  
```  
  
## Return Value  
 A reference to the basic_ostream object.  
  
## Remarks  
 If [rdbuf](../vs140/basic_ios--rdbuf.md) is not a null pointer, the function calls **rdbuf->**[pubsync](../vs140/basic_streambuf--pubsync.md). If that returns -1, the function calls [setstate](../vs140/basic_ios--setstate.md)(**badbit**). It returns **\*this**.  
  
## Example  
  
```  
// basic_ostream_flush.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   cout << "test";  
   cout.flush();  
}  
```  
  
 **test**   
## Requirements  
 **Header:** <ostream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ostream Class](../vs140/basic_ostream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)