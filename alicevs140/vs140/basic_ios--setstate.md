---
title: "basic_ios::setstate"
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
ms.assetid: 9c97d659-fafa-46dd-8933-afa719d70bbe
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ios::setstate
Sets additional flags.  
  
## Syntax  
  
```  
  
      void setstate(  
   iostate _State  
);  
```  
  
#### Parameters  
 `_State`  
 Additional flags to set.  
  
## Remarks  
 The member function effectively calls [clear](../vs140/basic_ios--clear.md)(_*State* &#124; [rdstate](../vs140/basic_ios--rdstate.md)).  
  
## Example  
  
```  
// basic_ios_setstate.cpp  
// compile with: /EHsc  
#include <ios>  
#include <iostream>  
using namespace std;  
  
int main( )   
{  
   bool b = cout.bad( );  
   cout << b << endl;   // Good  
   cout.clear( ios::badbit );  
   b = cout.bad( );  
   // cout.clear( );  
   cout << b << endl;   // Is bad, good  
   b = cout.fail( );  
   cout << b << endl;   // Not failed  
   cout.setstate( ios::failbit );  
   b = cout.fail( );  
   cout.clear( );  
   cout << b << endl;   // Is failed, good  
   return 0;  
}  
```  
  
 **0**  
**1**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)