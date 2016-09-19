---
title: "not"
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
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: d2ddbd5c-33c0-4aff-8961-feac155b4ba1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# not
An alternative to the ! operator.  
  
## Syntax  
  
```  
  
#define not !  
  
```  
  
## Remarks  
 The macro yields the operator !.  
  
## Example  
  
```  
// iso646_not.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iso646.h>  
  
int main( )  
{  
   using namespace std;  
   int a = 0;  
  
   if (!a)  
      cout << "a is zero" << endl;  
  
   if (not(a))  
      cout << "a is zero" << endl;  
}  
```  
  
 **a is zero**  
**a is zero**   
## Requirements  
 **Header:** <iso646.h>