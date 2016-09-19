---
title: "numeric_limits::has_signaling_NaN"
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
ms.assetid: 54f23292-945b-4bcd-aec7-ff43fbd9577b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numeric_limits::has_signaling_NaN
Tests whether a type has a representation for signaling not a number (NAN).  
  
## Syntax  
  
```  
  
static const bool has_signaling_NaN = false;  
  
```  
  
## Return Value  
 **true** if the type has a representation for a signaling NAN; **false** if not.  
  
## Remarks  
 A signaling NAN is an encoding for not a number, which signals its presence in an expression. The return value is **true** [is_iec559](../vs140/numeric_limits--is_iec559.md) is true.  
  
## Example  
  
```  
// numeric_limits_has_signaling_nan.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <limits>  
  
using namespace std;  
  
int main( )  
{  
   cout << "Whether float objects have a signaling_NaN: "  
        << numeric_limits<float>::has_signaling_NaN   
        << endl;  
   cout << "Whether double objects have a signaling_NaN: "  
        << numeric_limits<double>::has_signaling_NaN   
        << endl;  
   cout << "Whether long int objects have a signaling_NaN: "   
        << numeric_limits<long int>::has_signaling_NaN   
        << endl;  
}  
```  
  
 **Whether float objects have a signaling_NaN: 1**  
**Whether double objects have a signaling_NaN: 1**  
**Whether long int objects have a signaling_NaN: 0**   
## Requirements  
 **Header:** <limits\>  
  
 **Namespace:** std  
  
## See Also  
 [strstreambuf Class](../vs140/strstreambuf-Class.md)