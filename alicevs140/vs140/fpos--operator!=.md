---
title: "fpos::operator!="
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
ms.assetid: 451d908a-7a10-487d-9e20-7ffb431e3736
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fpos::operator!=
Tests file-position indicators for inequality.  
  
## Syntax  
  
```  
bool operator!=(  
    const fpos<Statetype>& _Right  
) const;  
```  
  
#### Parameters  
 `_Right`  
 The file-position indicator against which to compare.  
  
## Return Value  
 **true** if the file-position indicators are not equal, otherwise **false**.  
  
## Remarks  
 The member function returns **!**(**\*this ==** `_Right`).  
  
## Example  
  
```  
// fpos_op_neq.cpp  
// compile with: /EHsc  
#include <fstream>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   fpos<int> pos1, pos2;  
   ifstream file;  
   char c;  
  
   // Compare two fpos object  
   if ( pos1 != pos2 )  
      cout << "File position pos1 and pos2 are not equal" << endl;  
   else  
      cout << "File position pos1 and pos2 are equal" << endl;  
  
   file.open( "fpos_op_neq.txt" );  
   file.seekg( 0 );   // Goes to a zero-based position in the file  
   pos1 = file.tellg( );  
   file.get( c);  
   cout << c << endl;  
  
   // Increment pos1  
   pos1 += 1;  
   file.get( c );  
   cout << c << endl;  
  
   pos1 = file.tellg( ) - fpos<int>( 2);  
   file.seekg( pos1 );  
   file.get( c );  
   cout << c << endl;  
  
   // Increment pos1  
   pos1 = pos1 + fpos<int>( 1 );  
   file.get(c);  
   cout << c << endl;  
  
   pos1 -= fpos<int>( 2 );  
   file.seekg( pos1 );  
   file.get( c );  
   cout << c << endl;  
  
   file.close( );  
}  
```  
  
## Input: fpos_op_neq.txt  
  
```  
987654321  
```  
  
### Output  
  
```  
File position pos1 and pos2 are equal  
9  
8  
9  
8  
8  
```  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [fpos Class](../vs140/fpos-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)