---
title: "Compiler Error C3373"
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
ms.assetid: 6e7586c3-1a15-4773-ad20-f90090a400dc
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3373
attribute 'attribute' takes no arguments except on a coclass  
  
 Some attributes can be applied to more than one C++ construct, but arguments to the attribute may only be allowed on some constructs.  
  
 The following sample generates C3373:  
  
```  
// C3373.cpp  
#include <windows.h>  
  
[module(name="MyModule")];  
  
[ object, uuid(373a1a4c-469b-11d3-a6b0-00c04f79ae8f) ]  
__interface IMyIface  
{  
   // arguments to source and restricted are not allowed when  
   // these attributes are applied to an interface  
   [source(IMyIface)] HRESULT f1();  
   [restricted(IMyIface)] HRESULT f2(); // C3373  
};  
  
[ coclass, uuid(373a1a4d-469b-11d3-a6b0-00c04f79ae8f) ]  
class CMyClass : public IMyIface {  
};  
  
int main() {  
}  
```