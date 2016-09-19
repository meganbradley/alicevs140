---
title: "isnan, _isnan, _isnanf"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _isnan
  - _isnanf
  - isnan
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr90.dll
  - api-ms-win-crt-math-l1-1-0.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: 391fbc5b-89a4-4fba-997e-68f1131caf82
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# isnan, _isnan, _isnanf
Tests if a floating-point value is not a number (NAN).  
  
## Syntax  
  
```  
int isnan(  
   /* floating-point */ x   
); /* C-only macro */  
  
int _isnan(  
   double x   
);  
  
int _isnanf(  
   float x  
); /* x64 only */  
  
template <class T>  
bool isnan(  
   T x  
) throw(); /* C++ only */  
```  
  
#### Parameters  
 *x*  
 The floating-point value to test.  
  
## Return Value  
 In C, the `isnan` macro and the `_isnan` and `_isnanf` functions return a nonzero value if the argument `x` is a NAN; otherwise they return 0.  
  
 In C++, the `isnan` template functions return `true` if the argument `x` is a NAN; otherwise they return `false`.  
  
## Remarks  
 The C `isnan` macro and the `_isnan` and `_isnanf` functions test floating-point value *x*, returning a nonzero value if *x* is a Not a Number (NAN) value. A NAN is generated when the result of a floating-point operation can't be represented in IEEE-754 floating-point format for the specified type. For information about how a NAN is represented for output, see [printf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md).  
  
 When compiled as C++, the `isnan` macro is not defined, and an `isnan` template function is defined instead. It returns a value of type `bool` instead of an integer.  
  
 The `_isnan` and `_isnanf` functions are Microsoft specific. The `_isnanf` function is only available when compiled for x64.  
  
## Requirements  
  
|Routine|Required header (C)|Required header (C++)|  
|-------------|---------------------------|-------------------------------|  
|`isnan`, `_isnanf`|<math.h>|<math.h> or <cmath\>|  
|`_isnan`|<float.h>|<float.h> or <cfloat\>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [_finite, _finitef](../vs140/_finite--_finitef.md)   
 [_fpclass, _fpclassf](../vs140/_fpclass--_fpclassf.md)