---
title: "basic_ios::rdbuf"
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
ms.assetid: 960139bd-cf89-418e-887c-8463e5799416
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ios::rdbuf
Routes stream to specified buffer.  
  
## Syntax  
  
```  
basic_streambuf<Elem, Traits> *rdbuf( ) const;  
basic_streambuf<Elem, Traits> *rdbuf(   
    basic_streambuf<Elem, Traits> *_Sb  
);  
```  
  
#### Parameters  
 `_Sb`  
 A stream.  
  
## Remarks  
 The first member function returns the stored stream buffer pointer.  
  
 The second member function stores `_Sb` in the stored stream buffer pointer and returns the previously stored value.  
  
## Example  
  
```  
// basic_ios_rdbuf.cpp  
// compile with: /EHsc  
#include <ios>  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
   ofstream file( "rdbuf.txt" );  
   streambuf *x = cout.rdbuf( file.rdbuf( ) );  
   cout << "test" << endl;   // Goes to file  
   cout.rdbuf(x);  
   cout << "test2" << endl;  
}  
```  
  
 **test2**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)