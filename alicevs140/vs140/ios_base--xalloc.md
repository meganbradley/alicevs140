---
title: "ios_base::xalloc"
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
ms.assetid: 302f8773-f86b-4517-8690-ec6ed1e82c59
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::xalloc
Specifies that a variable is part of the stream.  
  
## Syntax  
  
```  
  
static int xalloc( );  
  
```  
  
## Return Value  
 The static member function returns a stored static value, which it increments on each call.  
  
## Remarks  
 You can use the return value as a unique index argument when calling the member functions [iword](../vs140/ios_base--iword.md) or [pword](../vs140/ios_base--pword.md).  
  
## Example  
  
```  
// ios_base_xalloc.cpp  
// compile with: /EHsc  
// Lets you store user-defined information.  
// iword, jword, xalloc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
  
   static const int i = ios_base::xalloc();  
   static const int j = ios_base::xalloc();  
   cout.iword( i ) = 11;  
   cin.iword( i ) = 13;  
   cin.pword( j ) = "testing";  
   cout << cout.iword( i ) << endl;  
   cout << cin.iword( i ) << endl;  
   cout << ( char * )cin.pword( j ) << endl;  
}  
```  
  
 **11**  
**13**  
**testing**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)