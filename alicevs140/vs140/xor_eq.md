---
title: "xor_eq"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apilocation: 
  - msvcr120.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: eca4b6b4-b77a-4d44-a09a-5a7e69fdb56c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# xor_eq
An alternative to the ^= operator.  
  
## Syntax  
  
```  
  
#define xor_eq ^=  
  
```  
  
## Remarks  
 The macro yields the operator ^=.  
  
## Example  
  
```  
// iso646_xor_eq.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iso646.h>  
  
int main( )  
{  
   using namespace std;  
   int a = 3, b = 2, result;  
  
   result= a ^= b;  
   cout << result << endl;  
  
   a = 3;  
   b = 2;  
  
   result= a xor_eq b;  
   cout << result << endl;  
}  
```  
  
 **1**  
**1**   
## Requirements  
 **Header:** <iso646.h>