---
title: "numeric_limits::round_error"
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
ms.assetid: ebb81161-df01-47de-8c46-70234381ff7b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numeric_limits::round_error
Returns the maximum rounding error for the type.  
  
## Syntax  
  
```  
  
static Type round_error( ) throw( );  
  
```  
  
## Return Value  
 The maximum rounding error for the type.  
  
## Example  
  
```  
// numeric_limits_round_error.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <limits>  
  
using namespace std;  
  
int main( )  
{  
   cout << "The maximum rounding error for type float is:  "  
        << numeric_limits<float>::round_error( )  
        << endl;  
   cout << "The maximum rounding error for type int is:  "  
        << numeric_limits<int>::round_error( )  
        << endl;  
   cout << "The maximum rounding error for type long double is:  "  
        << numeric_limits<long double>::round_error( )  
        << endl;  
}  
```  
  
 **The maximum rounding error for type float is:  0.5**  
**The maximum rounding error for type int is:  0**  
**The maximum rounding error for type long double is:  0.5**   
## Requirements  
 **Header:** <limits\>  
  
 **Namespace:** std  
  
## See Also  
 [strstreambuf Class](../vs140/strstreambuf-Class.md)