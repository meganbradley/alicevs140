---
title: "Compiler Error C3732"
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
ms.topic: error-reference
ms.assetid: 2d55a7e1-9c39-4379-a093-2f7beb27e2ca
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3732
'interface': a custom interface that fires COM events cannot inherit from IDispatch  
  
 An interface that supports COM events cannot inherit from `IDispatch`. For more information, see [Event Handling in COM](../vs140/Event-Handling-in-COM.md).  
  
 The following error generates C3732:  
  
```  
// C3732.cpp  
#define _ATL_ATTRIBUTES 1  
#include "atlbase.h"  
#include "atlcom.h"  
  
[module(name="test")];  
  
// to resolve this C3732, use dual instead of object  
// or inherit from IUnknown  
[ object ]  
__interface I : IDispatch  
{  
};  
  
[ event_source(com), coclass ]  
struct A  
{  
   __event __interface I;   // C3732  
};  
  
int main()  
{  
}  
```