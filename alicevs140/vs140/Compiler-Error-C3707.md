---
title: "Compiler Error C3707"
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
ms.assetid: ac63a5dd-7a4b-48d2-9f2a-be9cb090134c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3707
'function' : dispinterface method must have a dispid  
  
 If you use a `dispinterface` method, you must assign it a `dispid`. To fix this error, assign a `dispid` to the `dispinterface` method, for example, by uncommenting the `id` attribute on the method in the sample below. For more information, see the attributes [dispinterface](../vs140/dispinterface.md) and [id](../vs140/id.md).  
  
 The following sample generates C3707:  
  
```  
// C3707.cpp  
#include <atlbase.h>  
#include <atlcom.h>  
#include <atlctl.h>  
  
[module(name="xx")];  
[dispinterface]  
__interface IEvents : IDispatch  
{  
   HRESULT event1([in] int i);   // C3707  
   // try the following line instead  
   // [id(1)] HRESULT event1([in] int i);  
};  
  
int main() {  
}  
```