---
title: "basic_streambuf::stossc"
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
ms.assetid: c8d8e16b-668c-49d4-90fb-9fe32f400887
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::stossc
Move past the current element in the stream.  
  
## Syntax  
  
```  
  
void stossc( );  
  
```  
  
## Remarks  
 The member function calls [sbumpc](../vs140/basic_streambuf--sbumpc.md). Note that an implementation is not required to supply this member function.  
  
## Example  
  
```  
// basic_streambuf_stossc.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
   ifstream myfile( "basic_streambuf_stossc.txt", ios::in );  
  
   myfile.rdbuf( )->stossc( );  
   char i = myfile.rdbuf( )->sgetc( );  
   cout << i << endl;  
}  
```  
  
## Input: basic_streambuf_stossc.txt  
  
```  
testing  
```  
  
### Output  
  
```  
e  
```  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)