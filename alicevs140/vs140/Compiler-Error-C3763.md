---
title: "Compiler Error C3763"
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
ms.assetid: 58b1f079-cd1d-46e0-9431-ea18210106b7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3763
'type': 'retval' and 'out' can only appear on a data-pointer type  
  
 The [out](../vs140/out--C---.md) or [retval](../vs140/retval.md) attributes can only appear on parameters of type pointer. Either remove the attribute or make the parameter of type pointer.  
  
 The following sample generates C3763:  
  
```  
// C3763.cpp  
#define _ATL_ATTRIBUTES 1  
#include <atlbase.h>  
#include <atlplus.h>  
#include <atlcom.h>  
  
[ module(name=test) ];  
  
[ dispinterface, uuid("00000000-0000-0000-0000-000000000001") ]  
__interface IF84 : IDispatch  
{  
   [id(0x00000002)]HRESULT m2([out]unsigned char);  
};  
  
[ coclass, uuid("00000000-0000-0000-0000-000000000002") ]  
class CF84 : public IF84  
{   // C3763  
public:  
   HRESULT __stdcall m2(unsigned char i)  
   {  
      return S_OK;  
   }  
};  
  
int main()  
{  
}  
```