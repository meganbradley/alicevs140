---
title: "Concurrency::precise_math Namespace"
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
ms.topic: article
ms.assetid: ba653308-dc28-4384-b2fd-6cd718a72f91
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Concurrency::precise_math Namespace
Functions in the `precise_math` namespace are C99 compliant. Both single precision and double precision versions of each function are included. For example, `acos` is the double-precision version and `acosf` is the single-precision version. These functions, including the single-precision functions, require extended double-precision support on the accelerator. You can use the [accelerator::supports_double_precision Data Member](../vs140/accelerator--supports_double_precision-Data-Member.md) to determine if you can run these functions on a specific accelerator.  
  
## Syntax  
  
```cpp  
namespace precise_math;  
```  
  
#### Parameters  
  
## Members  
  
### Functions  
  
|Name|Description|  
|----------|-----------------|  
|[acos Function](../vs140/acos-Function.md)|Overloaded. Calculates the arccosine of the argument|  
|[acosf Function](../vs140/acosf-Function.md)|Calculates the arccosine of the argument|  
|[acosh Function](../vs140/acosh-Function.md)|Overloaded. Calculates the inverse hyperbolic cosine of the argument|  
|[acoshf Function](../vs140/acoshf-Function.md)|Calculates the inverse hyperbolic cosine of the argument|  
|[asin Function](../vs140/asin-Function.md)|Overloaded. Calculates the arcsine of the argument|  
|[asinf Function](../vs140/asinf-Function.md)|Calculates the arcsine of the argument|  
|[asinh Function](../vs140/asinh-Function.md)|Overloaded. Calculates the inverse hyperbolic sine of the argument|  
|[asinhf Function](../vs140/asinhf-Function.md)|Calculates the inverse hyperbolic sine of the argument|  
|[atan Function](../vs140/atan-Function.md)|Overloaded. Calculates the arctangent of the argument|  
|[atan2 Function](../vs140/atan2-Function.md)|Overloaded. Calculates the arctangent of _Y/_X|  
|[atan2f Function](../vs140/atan2f-Function.md)|Calculates the arctangent of _Y/_X|  
|[atanf Function](../vs140/atanf-Function.md)|Calculates the arctangent of the argument|  
|[atanh Function](../vs140/atanh-Function.md)|Overloaded. Calculates the inverse hyperbolic tangent of the argument|  
|[atanhf Function](../vs140/atanhf-Function.md)|Calculates the inverse hyperbolic tangent of the argument|  
|[cbrt Function](../vs140/cbrt-Function.md)|Overloaded. Computes the real cube root of the argument|  
|[cbrtf Function](../vs140/cbrtf-Function.md)|Computes the real cube root of the argument|  
|[ceil Function](../vs140/ceil-Function.md)|Overloaded. Calculates the ceiling of the argument|  
|[ceilf Function](../vs140/ceilf-Function.md)|Calculates the ceiling of the argument|  
|[copysign Function](../vs140/copysign-Function.md)|Overloaded. Produces a value with the magnitude of _X and the sign of _Y|  
|[copysignf Function](../vs140/copysignf-Function.md)|Produces a value with the magnitude of _X and the sign of _Y|  
|[cos Function](../vs140/cos-Function.md)|Overloaded. Calculates the cosine of the argument|  
|[cosf Function](../vs140/cosf-Function.md)|Calculates the cosine of the argument|  
|[cosh Function](../vs140/cosh-Function.md)|Overloaded. Calculates the hyperbolic cosine value of the argument|  
|[coshf Function](../vs140/coshf-Function.md)|Calculates the hyperbolic cosine value of the argument|  
|[cospi Function](../vs140/cospi-Function.md)|Overloaded. Calculates the cosine value of pi * _X|  
|[cospif Function](../vs140/cospif-Function.md)|Calculates the cosine value of pi * _X|  
|[erf Function](../vs140/erf-Function.md)|Overloaded. Computes the error function of _X|  
|[erfc Function](../vs140/erfc-Function.md)|Overloaded. Computes the complementary error function of _X|  
|[erfcf Function](../vs140/erfcf-Function.md)|Computes the complementary error function of _X|  
|[erfcinv Function](../vs140/erfcinv-Function.md)|Overloaded. Computes the inverse complementary error function of _X|  
|[erfcinvf Function](../vs140/erfcinvf-Function.md)|Computes the inverse complementary error function of _X|  
|[erff Function](../vs140/erff-Function.md)|Computes the error function of _X|  
|[erfinv Function](../vs140/erfinv-Function.md)|Overloaded. Computes the inverse error function of _X|  
|[erfinvf Function](../vs140/erfinvf-Function.md)|Computes the inverse error function of _X|  
|[exp Function](../vs140/exp-Function.md)|Overloaded. Calculates the base-e exponential of the argument|  
|[exp10 Function](../vs140/exp10-Function.md)|Overloaded. Calculates the base-10 exponential of the argument|  
|[exp10f Function](../vs140/exp10f-Function.md)|Calculates the base-10 exponential of the argument|  
|[exp2 Function](../vs140/exp2-Function.md)|Overloaded. Calculates the base-2 exponential of the argument|  
|[exp2f Function](../vs140/exp2f-Function.md)|Calculates the base-2 exponential of the argument|  
|[expf Function](../vs140/expf-Function.md)|Calculates the base-e exponential of the argument|  
|[expm1 Function](../vs140/expm1-Function.md)|Overloaded. Calculates the base-e exponential of the argument, minus 1|  
|[expm1f Function](../vs140/expm1f-Function.md)|Calculates the base-e exponential of the argument, minus 1|  
|[fabs Function](../vs140/fabs-Function.md)|Overloaded. Returns the absolute value of the argument|  
|[fabsf Function](../vs140/fabsf-Function.md)|Returns the absolute value of the argument|  
|[fdim Function](../vs140/fdim-Function.md)|Overloaded. Determines the positive difference between the arguments|  
|[fdimf Function](../vs140/fdimf-Function.md)|Determines the positive difference between the arguments|  
|[floor Function](../vs140/floor-Function.md)|Overloaded. Calculates the floor of the argument|  
|[floorf Function](../vs140/floorf-Function.md)|Calculates the floor of the argument|  
|[fma Function](../vs140/fma-Function.md)|Overloaded. Compute (_X * _Y) + _Z, rounded as one ternary operation|  
|[fmaf Function](../vs140/fmaf-Function.md)|Compute (_X * _Y) + _Z, rounded as one ternary operation|  
|[fmax Function](../vs140/fmax-Function.md)|Overloaded. Determine the maximum numeric value of the arguments|  
|[fmaxf Function](../vs140/fmaxf-Function.md)|Determine the maximum numeric value of the arguments|  
|[fmin Function](../vs140/fmin-Function.md)|Overloaded. Determine the minimum numeric value of the arguments|  
|[fminf Function](../vs140/fminf-Function.md)|Determine the minimum numeric value of the arguments|  
|[fmod Function (C++ AMP)](../vs140/fmod-Function--C---AMP-.md)|Overloaded. Calculates the floating-point remainder of _X/_Y|  
|[fmodf Function](../vs140/fmodf-Function.md)|Calculates the floating-point remainder of _X/_Y|  
|[fpclassify Function](../vs140/fpclassify-Function.md)|Overloaded. Classifies the argument value as NaN, infinite, normal, subnormal, zero|  
|[frexp Function](../vs140/frexp-Function.md)|Overloaded. Gets the mantissa and exponent of _X|  
|[frexpf Function](../vs140/frexpf-Function.md)|Gets the mantissa and exponent of _X|  
|[hypot Function](../vs140/hypot-Function.md)|Overloaded. Computes the square root of the sum of the squares of _X and _Y|  
|[hypotf Function](../vs140/hypotf-Function.md)|Computes the square root of the sum of the squares of _X and _Y|  
|[ilogb Function](../vs140/ilogb-Function.md)|Overloaded. Extract the exponent of _X as a signed int value|  
|[ilogbf Function](../vs140/ilogbf-Function.md)|Extract the exponent of _X as a signed int value|  
|[isfinite Function](../vs140/isfinite-Function.md)|Overloaded. Determines whether the argument has a finite value|  
|[isinf Function](../vs140/isinf-Function.md)|Overloaded. Determines whether the argument is an infinity|  
|[isnan Function](../vs140/isnan-Function.md)|Overloaded. Determines whether the argument is a NaN|  
|[isnormal Function](../vs140/isnormal-Function.md)|Overloaded. Determines whether the argument is a normal|  
|[ldexp Function](../vs140/ldexp-Function.md)|Overloaded. Computes a real number from the mantissa and exponent|  
|[ldexpf Function](../vs140/ldexpf-Function.md)|Computes a real number from the mantissa and exponent|  
|[lgamma Function](../vs140/lgamma-Function.md)|Overloaded. Computes the natural logarithm of the absolute value of gamma of the argument|  
|[lgammaf Function](../vs140/lgammaf-Function.md)|Computes the natural logarithm of the absolute value of gamma of the argument|  
|[log Function](../vs140/log-Function.md)|Overloaded. Calculates the base-e logarithm of the argument|  
|[log10 Function](../vs140/log10-Function.md)|Overloaded. Calculates the base-10 logarithm of the argument|  
|[log10f Function](../vs140/log10f-Function.md)|Calculates the base-10 logarithm of the argument|  
|[log1p Function](../vs140/log1p-Function.md)|Overloaded. Calculates the base-e logarithm of 1 plus the argument|  
|[log1pf Function](../vs140/log1pf-Function.md)|Calculates the base-e logarithm of 1 plus the argument|  
|[log2 Function](../vs140/log2-Function.md)|Overloaded. Calculates the base-2 logarithm of the argument|  
|[log2f Function](../vs140/log2f-Function.md)|Calculates the base-2 logarithm of the argument|  
|[logb Function](../vs140/logb-Function.md)|Overloaded. Extracts the exponent of _X, as a signed integer value in floating-point format|  
|[logbf Function](../vs140/logbf-Function.md)|Extracts the exponent of _X, as a signed integer value in floating-point format|  
|[logf Function](../vs140/logf-Function.md)|Calculates the base-e logarithm of the argument|  
|[modf Function](../vs140/modf-Function.md)|Overloaded. Splits _X into fractional and integer parts.|  
|[modff Function](../vs140/modff-Function.md)|Splits _X into fractional and integer parts.|  
|[nan Function](../vs140/nan-Function.md)|Returns a quiet NaN|  
|[nanf Function](../vs140/nanf-Function.md)|Returns a quiet NaN|  
|[nearbyint Function](../vs140/nearbyint-Function.md)|Overloaded. Rounds the argument to an integer value in floating-point format, using the current rounding direction.|  
|[nearbyintf Function](../vs140/nearbyintf-Function.md)|Rounds the argument to an integer value in floating-point format, using the current rounding direction.|  
|[nextafter Function](../vs140/nextafter-Function.md)|Overloaded. Determine the next representable value, in the type of the function, after _X in the direction of _Y|  
|[nextafterf Function](../vs140/nextafterf-Function.md)|Determine the next representable value, in the type of the function, after _X in the direction of _Y|  
|[phi Function](../vs140/phi-Function.md)|Overloaded. Returns the cumulative distribution function of the argument|  
|[phif Function](../vs140/phif-Function.md)|Returns the cumulative distribution function of the argument|  
|[pow Function](../vs140/pow-Function.md)|Overloaded. Calculates _X raised to the power of _Y|  
|[powf Function](../vs140/powf-Function.md)|Calculates _X raised to the power of _Y|  
|[probit Function](../vs140/probit-Function.md)|Overloaded. Returns the inverse cumulative distribution function of the argument|  
|[probitf Function](../vs140/probitf-Function.md)|Returns the inverse cumulative distribution function of the argument|  
|[rcbrt Function](../vs140/rcbrt-Function.md)|Overloaded. Returns the reciprocal of the cube root of the argument|  
|[rcbrtf Function](../vs140/rcbrtf-Function.md)|Returns the reciprocal of the cube root of the argument|  
|[remainder Function](../vs140/remainder-Function.md)|Overloaded. Computes the remainder: _X REM _Y|  
|[remainderf Function](../vs140/remainderf-Function.md)|Computes the remainder: _X REM _Y|  
|[remquo Function](../vs140/remquo-Function.md)|Overloaded. Computes the same remainder as _X REM _Y. Also calculates the lower 23 bits of the integral quotient _X/_Y, and gives that value the same sign as _X/_Y. It stores this signed value in the integer pointed to by _Quo.|  
|[remquof Function](../vs140/remquof-Function.md)|Computes the same remainder as _X REM _Y. Also calculates the lower 23 bits of the integral quotient _X/_Y, and gives that value the same sign as _X/_Y. It stores this signed value in the integer pointed to by _Quo.|  
|[round Function](../vs140/round-Function.md)|Overloaded. Rounds _X to the nearest integer|  
|[roundf Function](../vs140/roundf-Function.md)|Rounds _X to the nearest integer|  
|[rsqrt Function](../vs140/rsqrt-Function.md)|Overloaded. Returns the reciprocal of the square root of the argument|  
|[rsqrtf Function](../vs140/rsqrtf-Function.md)|Returns the reciprocal of the square root of the argument|  
|[scalb Function](../vs140/scalb-Function.md)|Overloaded. Multiplies _X by FLT_RADIX to the power _Y|  
|[scalbf Function](../vs140/scalbf-Function.md)|Multiplies _X by FLT_RADIX to the power _Y|  
|[scalbn Function](../vs140/scalbn-Function.md)|Overloaded. Multiplies _X by FLT_RADIX to the power _Y|  
|[scalbnf Function](../vs140/scalbnf-Function.md)|Multiplies _X by FLT_RADIX to the power _Y|  
|[signbit Function](../vs140/signbit-Function.md)|Overloaded. Determines whether the sign of _X is negative|  
|[signbitf Function](../vs140/signbitf-Function.md)|Determines whether the sign of _X is negative|  
|[sin Function](../vs140/sin-Function.md)|Overloaded. Calculates the sine value of the argument|  
|[sincos Function](../vs140/sincos-Function.md)|Overloaded. Calculates sine and cosine value of _X|  
|[sincosf Function](../vs140/sincosf-Function.md)|Calculates sine and cosine value of _X|  
|[sinf Function](../vs140/sinf-Function.md)|Calculates the sine value of the argument|  
|[sinh Function](../vs140/sinh-Function.md)|Overloaded. Calculates the hyperbolic sine value of the argument|  
|[sinhf Function](../vs140/sinhf-Function.md)|Calculates the hyperbolic sine value of the argument|  
|[sinpi Function](../vs140/sinpi-Function.md)|Overloaded. Calculates the sine value of pi * _X|  
|[sinpif Function](../vs140/sinpif-Function.md)|Calculates the sine value of pi * _X|  
|[sqrt Function](../vs140/sqrt-Function.md)|Overloaded. Calculates the squre root of the argument|  
|[sqrtf Function](../vs140/sqrtf-Function.md)|Calculates the squre root of the argument|  
|[tan Function](../vs140/tan-Function.md)|Overloaded. Calculates the tangent value of the argument|  
|[tanf Function](../vs140/tanf-Function.md)|Calculates the tangent value of the argument|  
|[tanh Function](../vs140/tanh-Function.md)|Overloaded. Calculates the hyperbolic tangent value of the argument|  
|[tanhf Function](../vs140/tanhf-Function.md)|Calculates the hyperbolic tangent value of the argument|  
|[tanpi Function](../vs140/tanpi-Function.md)|Overloaded. Calculates the tangent value of pi * _X|  
|[tanpif Function](../vs140/tanpif-Function.md)|Calculates the tangent value of pi * _X|  
|[tgamma Function](../vs140/tgamma-Function.md)|Overloaded. Computes the gamma function of _X|  
|[tgammaf Function](../vs140/tgammaf-Function.md)|Computes the gamma function of _X|  
|[trunc Function](../vs140/trunc-Function.md)|Overloaded. Truncates the argument to the integer component|  
|[truncf Function](../vs140/truncf-Function.md)|Truncates the argument to the integer component|  
  
## Requirements  
 **Header:** amp_math.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace (C++ AMP)](../vs140/Concurrency-Namespace--C---AMP-.md)