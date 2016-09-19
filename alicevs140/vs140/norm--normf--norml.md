---
title: "norm, normf, norml"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - cpp
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - norm
  - normf
  - norml
apilocation: 
  - msvcr120.dll
  - api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
ms.assetid: 9786ecfe-0019-4553-b378-0af6c691e15c
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# norm, normf, norml
Retrieves the squared magnitude of a complex number.  
  
## Syntax  
  
```  
double norm(   
   _Dcomplex z   
);  
float norm(   
   _Fcomplex z   
);  // C++ only  
long double norm(   
  _Lcomplex z   
);  // C++ only  
float normf(   
   _Fcomplex z   
);  
long double norml(   
   _Lcomplex z   
);  
```  
  
#### Parameters  
 `z`  
 A complex number.  
  
## Return Value  
 The squared magnitude of `z`.  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `norm` that take `_Fcomplex` or `_Lcomplex` values, and return `float` or `long double` values. In a C program, `norm` always takes a `_Dcomplex` value and returns a `double` value.  
  
## Requirements  
  
|Routine|C header|C++ header|  
|-------------|--------------|------------------|  
|`norm`,               `normf`, `norml`|<complex.h>|<ccomplex\>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## See Also  
 [CRT Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [creal, crealf, creall](../vs140/creal--crealf--creall.md)   
 [cproj, cprojf, cprojl](../vs140/cproj--cprojf--cprojl.md)   
 [conj, conjf, conjl](../vs140/conj--conjf--conjl.md)   
 [cimag, cimagf, cimagl](../vs140/cimag--cimagf--cimagl.md)   
 [carg, cargf, cargl](../vs140/carg--cargf--cargl.md)   
 [cabs, cabsf, cabsl](../vs140/cabs--cabsf--cabsl.md)