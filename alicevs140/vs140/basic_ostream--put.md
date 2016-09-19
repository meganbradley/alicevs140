---
title: "basic_ostream::put"
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
ms.assetid: bc6dbce3-9f22-470c-a91f-89de7d2f80e8
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ostream::put
Puts a character in a stream.  
  
## Syntax  
  
```  
basic_ostream<_Elem, _Tr>& put(  
    char_type _Ch  
);  
```  
  
#### Parameters  
 `_Ch`  
 A character.  
  
## Return Value  
 A reference to the basic_ostream object.  
  
## Remarks  
 The unformatted output function inserts the element `_Ch`. It returns **\*this**.  
  
## Example  
  
```  
// basic_ostream_put.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   cout.put( 'v' );  
   cout << endl;  
   wcout.put( L'l' );  
}  
```  
  
 **v**  
**l**   
## Requirements  
 **Header:** <ostream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ostream Class](../vs140/basic_ostream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)