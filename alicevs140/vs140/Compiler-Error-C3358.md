---
title: "Compiler Error C3358"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 180b93df-e78f-441a-91fb-1594c681f7f0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3358
'symbol': symbol not found  
  
 The required symbol was not found.  
  
 The following sample generates C3358:  
  
```  
// C3358.cpp  
#define __ATLEVENT_H__ 1   // remove this line to resolve the error  
#define _ATL_ATTRIBUTES 1  
#include "atlbase.h"  
#include "atlcom.h"  
  
[event_receiver(com)]  
struct A   // C3358  
{  
   void func();  
};  
  
int main()  
{  
}  
```