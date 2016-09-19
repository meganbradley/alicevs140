---
title: "basic_ios::operator void *"
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
ms.assetid: d4843f16-7303-46ea-bc0e-afd84071426a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ios::operator void *
Indicates if the stream is still good.  
  
## Syntax  
  
```  
  
operator void *( ) const;  
  
```  
  
## Return Value  
 The operator returns a null pointer only if [fail](../vs140/basic_ios--fail.md).  
  
## Example  
  
```  
// basic_ios_opgood.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   cout << (bool)(&cout != 0) << endl;   // Stream is still good  
}  
```  
  
 **1**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)