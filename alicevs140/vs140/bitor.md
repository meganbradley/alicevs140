---
title: "bitor"
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
  - msvcr110.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 3c0a3711-9c74-41f2-b400-2f7797da30d1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bitor
An alternative to the &#124; operator.  
  
## Syntax  
  
```  
  
#define bitor |  
  
```  
  
## Remarks  
 The macro yields the operator &#124;.  
  
## Example  
  
```  
// iso646_bitor.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iso646.h>  
  
int main( )  
{  
   using namespace std;  
   int a = 1, b = 2, result;  
  
   result = a | b;  
   cout << result << endl;  
  
   result= a bitor b;  
   cout << result << endl;  
}  
```  
  
 **3**  
**3**   
## Requirements  
 **Header:** <iso646.h>