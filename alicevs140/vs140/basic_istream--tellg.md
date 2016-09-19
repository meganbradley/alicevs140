---
title: "basic_istream::tellg"
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
ms.assetid: b99be17d-e0d1-4177-ac4a-06d8ebd4110b
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_istream::tellg
Reports the current read position in the stream.  
  
## Syntax  
  
```  
  
pos  
_  
type tellg( );  
  
```  
  
## Return Value  
 The current position in the stream.  
  
## Remarks  
 If [fail](../vs140/basic_ios--fail.md) is false, the member function returns [rdbuf](../vs140/basic_ios--rdbuf.md) -> [pubseekoff](../vs140/basic_streambuf--pubseekoff.md)(0, `cur`, **in**). Otherwise, it returns `pos_type`(-1).  
  
## Example  
  
```  
// basic_istream_tellg.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main()  
{  
    using namespace std;  
    ifstream file;  
    char c;  
    streamoff i;  
  
    file.open("basic_istream_tellg.txt");  
    i = file.tellg();  
    file >> c;  
    cout << c << " " << i << endl;  
  
    i = file.tellg();  
    file >> c;  
    cout << c << " " << i << endl;  
}  
```  
  
## Input: basic_istream_tellg.txt  
  
```  
0123456789  
```  
  
## Program Output  
  
```  
0 0  
1 1  
```  
  
## Requirements  
 **Header:** <istream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_istream Class](../vs140/basic_istream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)