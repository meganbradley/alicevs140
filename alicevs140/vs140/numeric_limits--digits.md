---
title: "numeric_limits::digits"
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
ms.assetid: bc515ce2-da5c-4061-8400-577adaa929dc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numeric_limits::digits
Returns the number of radix digits that the type can represent without loss of precision.  
  
## Syntax  
  
```  
  
static const int digits = 0;  
  
```  
  
## Return Value  
 The number of radix digits that the type can represent without loss of precision.  
  
## Remarks  
 The member stores the number of radix digits that the type can represent without change, which is the number of bits other than any sign bit for a predefined integer type, or the number of mantissa digits for a predefined floating-point type.  
  
## Example  
  
```  
// numeric_limits_digits_min.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <limits>  
  
using namespace std;  
  
int main( )  
{  
   cout << numeric_limits<float>::digits <<endl;  
   cout << numeric_limits<double>::digits <<endl;  
   cout << numeric_limits<long double>::digits <<endl;  
   cout << numeric_limits<int>::digits <<endl;  
   cout << numeric_limits<__int64>::digits <<endl;  
}  
```  
  
 **24**  
**53**  
**53**  
**31**  
**63**   
## Requirements  
 **Header:** <limits\>  
  
 **Namespace:** std  
  
## See Also  
 [strstreambuf Class](../vs140/strstreambuf-Class.md)