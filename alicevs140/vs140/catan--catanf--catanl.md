---
title: "catan, catanf, catanl"
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
  - catan
  - catanf
  - catanl
apilocation: 
  - msvcr120.dll
  - api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
ms.assetid: 8415ed9c-7909-4d08-b532-4630bafdc7e8
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# catan, catanf, catanl
Retrieves the arctangent of a complex number with branch cuts outside the interval [−1; +1] along the imaginary axis.  
  
## Syntax  
  
```  
_Dcomplex catan(   
   _Dcomplex z   
);  
_Fcomplex catan(   
   _Fcomplex z   
);  // C++ only  
_Lcomplex catan(   
  _Lcomplex z   
);  // C++ only  
_Fcomplex catanf(   
   _Fcomplex z   
);  
_Lcomplex catanl(   
   _Lcomplex z   
);  
```  
  
#### Parameters  
 `z`  
 A complex number that represents an angle, in radians.  
  
## Return Value  
 The arctangent of `z`, in radians. The result is unbounded along the imaginary axis, and  in the interval [−π/2; +π/2] along the real axis.  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `catan` that take and return `_Fcomplex` and `_Lcomplex` values. In a C program, `catan` always takes and returns a `_Dcomplex` value.  
  
## Requirements  
  
|Routine|C header|C++ header|  
|-------------|--------------|------------------|  
|`catan`,               `catanf`, `catanl`|<complex.h>|<ccomplex\>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## See Also  
 [CRT Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [catanh, catanhf, catanhl](../vs140/catanh--catanhf--catanhl.md)   
 [ctanh, ctanhf, ctanhl](../vs140/ctanh--ctanhf--ctanhl.md)   
 [csinh, csinhf, csinhl](../vs140/csinh--csinhf--csinhl.md)   
 [casinh, casinhf, casinhl](../vs140/casinh--casinhf--casinhl.md)   
 [ccosh, ccoshf, ccoshl](../vs140/ccosh--ccoshf--ccoshl.md)   
 [cacosh, cacoshf, cacoshl](../vs140/cacosh--cacoshf--cacoshl.md)   
 [cacos, cacosf, cacosl](../vs140/cacos--cacosf--cacosl.md)   
 [ctan, ctanf, ctanl](../vs140/ctan--ctanf--ctanl.md)   
 [csin, csinf, csinl](../vs140/csin--csinf--csinl.md)   
 [casin, casinf, casinl](../vs140/casin--casinf--casinl.md)   
 [ccos, ccosf, ccosl](../vs140/ccos--ccosf--ccosl.md)   
 [csqrt, csqrtf, csqrtl](../vs140/csqrt--csqrtf--csqrtl.md)