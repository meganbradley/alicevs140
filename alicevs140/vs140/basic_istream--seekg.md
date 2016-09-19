---
title: "basic_istream::seekg"
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
ms.assetid: 0fd8591f-d0c0-4f25-8999-467d95ba2429
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_istream::seekg
Moves the read position in a stream.  
  
## Syntax  
  
```  
basic_istream<Elem, Tr>& seekg(  
    pos_type pos  
);  
basic_istream<Elem, Tr>& seekg(  
    off_type off,  
    ios_base::seekdir way  
);  
```  
  
#### Parameters  
 `pos`  
 The absolute position in which to move the read pointer.  
  
 `off`  
 An offset to move the read pointer relative to `way`.  
  
 `way`  
 One of the [ios_base::seekdir](../vs140/ios_base--seekdir.md) enumerations.  
  
## Return Value  
 The stream (**\*this**).  
  
## Remarks  
 The first member function performs an absolute seek, the second member function performs a relative seek.  
  
> [!NOTE]
>  Do not use the second member function with text files, because Standard C++ does not support relative seeks in text files.  
  
 If [fail](../vs140/basic_ios--fail.md) is false, the first member function calls **newpos** = [rdbuf](../vs140/basic_ios--rdbuf.md) -> [pubseekpos](../vs140/basic_streambuf--pubseekpos.md)(`pos`), for some **pos_type** temporary object **newpos**. If **fail** is false, the second function calls **newpos** = **rdbuf** -> [pubseekoff](../vs140/basic_streambuf--pubseekoff.md)(`off`, `way`). In either case, if (`off_type`)**newpos** == (`off_type`)(-1) (the positioning operation fails), the function calls **istr**.[setstate](../vs140/basic_ios--setstate.md)(**failbit**). Both functions return **\*this**.  
  
 If [fail](../vs140/basic_ios--fail.md) is true, the member functions do nothing.  
  
## Example  
  
```  
// basic_istream_seekg.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main ( )   
{  
   using namespace std;  
   ifstream file;  
   char c, c1;  
  
   file.open( "basic_istream_seekg.txt" );  
   file.seekg(2);   // seek to position 2  
   file >> c;  
   cout << c << endl;  
}  
```  
  
## Input: basic_istream_seekg.txt  
  
```  
0123456789  
```  
  
## Output  
  
```  
2  
```  
  
## Requirements  
 **Header:** <istream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_istream Class](../vs140/basic_istream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)