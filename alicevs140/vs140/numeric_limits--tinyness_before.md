---
title: "numeric_limits::tinyness_before"
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
ms.assetid: 2cb23ad1-2196-44fd-9d46-138f4eeee134
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numeric_limits::tinyness_before
Tests whether a type can determine that a value is too small to represent as a normalized value before rounding it.  
  
## Syntax  
  
```  
static const bool tinyness_before = false;  
```  
  
## Return Value  
 `true` if the type can detect tiny values before rounding; `false` if it cannot.  
  
## Remarks  
 Types that can detect tinyness were included as an option with IEC 559 floating-point representations and its implementation can affect some results.  
  
## Example  
  
```  
// numeric_limits_tinyness_before.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <limits>  
  
using namespace std;  
  
int main( )  
{  
   cout << "Whether float types can detect tinyness before rounding: "  
        << numeric_limits<float>::tinyness_before  
        << endl;  
   cout << "Whether double types can detect tinyness before rounding: "  
        << numeric_limits<double>::tinyness_before  
        << endl;  
   cout << "Whether long int types can detect tinyness before rounding: "  
        << numeric_limits<long int>::tinyness_before  
        << endl;  
   cout << "Whether unsigned char types can detect tinyness before rounding: "  
        << numeric_limits<unsigned char>::tinyness_before  
        << endl;  
}  
```  
  
 **Whether float types can detect tinyness before rounding: 1**  
**Whether double types can detect tinyness before rounding: 1**  
**Whether long int types can detect tinyness before rounding: 0**  
**Whether unsigned char types can detect tinyness before rounding: 0**   
## Requirements  
 **Header:** <limits\>  
  
 **Namespace:** std  
  
## See Also  
 [strstreambuf Class](../vs140/strstreambuf-Class.md)