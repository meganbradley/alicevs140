---
title: "ios_base::getloc"
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
ms.assetid: 3ae3a6a3-b3dd-4796-89cf-07478ca3da97
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::getloc
Returns the stored locale object.  
  
## Syntax  
  
```  
  
locale getloc( ) const;  
  
```  
  
## Return Value  
 The stored locale object.  
  
## Example  
  
```  
// ios_base_getlock.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   cout << cout.getloc( ).name( ).c_str( ) << endl;  
}  
```  
  
 **C**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)