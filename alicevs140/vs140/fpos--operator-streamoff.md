---
title: "fpos::operator streamoff"
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
ms.assetid: 476df952-8517-4fa0-abfd-1425469e7a21
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fpos::operator streamoff
Cast object of type `fpos` to object of type `streamoff`.  
  
## Syntax  
  
```  
operator streamoff( ) const;  
```  
  
## Remarks  
 The member function returns the stored offset member object and any additional offset stored as part of the `fpos_t` member object.  
  
## Example  
  
```  
// fpos_op_streampos.cpp  
// compile with: /EHsc  
#include <ios>  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
   streamoff s;  
   ofstream file( "rdbuf.txt");  
  
   fpos<mbstate_t> f = file.tellp( );  
   // Is equivalent to ..  
   // streampos f = file.tellp( );  
   s = f;  
   cout << s << endl;  
}  
```  
  
 **0**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [fpos Class](../vs140/fpos-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)