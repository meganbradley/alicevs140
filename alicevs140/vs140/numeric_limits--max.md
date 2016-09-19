---
title: "numeric_limits::max"
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
ms.assetid: 63e56dc3-fe13-4bcc-95d0-83d80f26b0f0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numeric_limits::max
Returns the maximum finite value for a type.  
  
## Syntax  
  
```  
  
static Type max( ) throw( );  
  
```  
  
## Return Value  
 The maximum finite value for a type.  
  
## Remarks  
 The maximum finite value is INT_MAX for type `int` and FLT_MAX for type **float**. The return value is meaningful if [is_bounded](../vs140/numeric_limits--is_bounded.md) is **true**.  
  
## Example  
  
```  
// numeric_limits_max.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <limits>  
  
using namespace std;  
  
int main() {  
   cout << "The maximum value for type float is:  "  
        << numeric_limits<float>::max( )  
        << endl;  
   cout << "The maximum value for type double is:  "  
        << numeric_limits<double>::max( )  
        << endl;  
   cout << "The maximum value for type int is:  "  
        << numeric_limits<int>::max( )  
        << endl;  
   cout << "The maximum value for type short int is:  "  
        << numeric_limits<short int>::max( )  
        << endl;  
}  
```  
  
## Output  
  
```  
The maximum value for type float is:  3.40282e+038  
The maximum value for type double is:  1.79769e+308  
The maximum value for type int is:  2147483647  
The maximum value for type short int is:  32767  
```  
  
## Requirements  
 **Header:** <limits\>  
  
 **Namespace:** std  
  
## See Also  
 [strstreambuf Class](../vs140/strstreambuf-Class.md)