---
title: "basic_ios::operator!"
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
ms.assetid: e6c523c7-768c-4376-8dc0-d5aef65b097b
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ios::operator!
Indicates if the stream is not bad.  
  
## Syntax  
  
```  
  
bool operator!( ) const;  
  
```  
  
## Return Value  
 Returns [fail](../vs140/basic_ios--fail.md).  
  
## Example  
  
```  
// basic_ios_opbad.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   cout << !cout << endl;   // Stream is not bad   
}  
```  
  
 **0**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)