---
title: "&lt;chrono&gt;"
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
ms.assetid: 844de749-f306-482e-89bc-6f53c99c8324
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;chrono&gt;
Include the standard header <chrono\> to define classes and functions that represent and manipulate time durations and time instants.  
  
 **(Visual Studio 2015:)** The implementation of `steady_clock` has changed to meet the C++ Standard requirements for steadiness and monotonicity. `steady_clock` is now based on QueryPerformanceCounter() and `high_resolution_clock` is now a typedef for `steady_clock`. As a result, in Visual C++ `steady_clock::time_point` is now a typedef for `chrono::time_point<steady_clock>`; however, this is not necessarily the case for other implementations.  
  
## Syntax  
  
```cpp  
#include <chrono>  
```  
  
### Literals  
 Literals in the <chrono\> header are members of the literals::chrono_literals inline namespace. For more information, see [chrono literals](../vs140/-chrono--functions.md#chrono_literals).  
  
|||  
|-|-|  
|operator "" h(unsigned long long Val) operator "" h(long double Val)|Specifies that the value represents hours.|  
|operator "" min(unsigned long long Val)  operator "" min(long double Val)|Specifies that the value represents minutes.|  
|operator "" s(unsigned long long Val)operator "" s(long double Val)|Specifies that the value represents seconds.|  
|operator "" ms(unsigned long long Val)operator "" ms(long double Val)|Specifies that the value represents milliseconds.|  
|operator "" us(unsigned long long Val)operator "" us(long double Val)|Specifies that the value represents microseconds.|  
|operator "" ns(unsigned long long Val)operator "" ns(long double Val)|Specifies that the value represents nanoseconds.|  
  
### Classes  
  
|Name|Description|  
|----------|-----------------|  
|[duration Class](../vs140/duration-Class.md)|Describes a type that holds a time interval.|  
|[time_point Class](../vs140/time_point-Class.md)|Describes a type that represents a point in time.|  
  
### Structs  
  
|Name|Description|  
|----------|-----------------|  
|[common_type Structure](../vs140/common_type-Structure.md)|Describes specializations of template class [common_type](../vs140/common_type-Class.md) for instantiations of `duration` and `time_point`.|  
|[duration_values Structure](../vs140/duration_values-Structure.md)|Provides specific values for the `duration` template parameter `Rep`.|  
|[steady_clock Class](../vs140/steady_clock-struct.md)|Represents a `steady` clock.|  
|[system_clock Structure](../vs140/system_clock-Structure.md)|Represents a *clock type* that is based on the real-time clock of the system.|  
|[treat_as_floating_point Structure](../vs140/treat_as_floating_point-Structure.md)|Specifies whether a type can be treated as a floating-point type.|  
  
### Functions  
  
|Name|Description|  
|----------|-----------------|  
|[duration_cast Function](../vs140/-chrono--functions.md#duration_cast_function)|Casts a `duration` object to a specified type.|  
|[time_point_cast Function](../vs140/-chrono--functions.md#time_point_cast_function)|Casts a `time_point` object to a specified type.|  
  
### Operators  
  
|Name|Description|  
|----------|-----------------|  
|[operator- Operator](../vs140/-chrono--operators.md#operator-)|Operator for subtraction or negation of `duration` and `time_point` objects.|  
|[operator!= Operator](../vs140/-chrono--operators.md#operator_neq)|Inequality operator that is used with `duration` or `time_point` objects.|  
|[operator% Operator](../vs140/-chrono--operators.md#operator_modulo)|Operator for modulo operations on `duration` objects.|  
|[operator* Operator](../vs140/-chrono--operators.md#operator_star)|Multiplication operator for `duration` objects.|  
|[operator/ Operator](../vs140/-chrono--operators.md#operator_)|Division operator for `duration` objects.|  
|[operator+ Operator](../vs140/-chrono--operators.md#operator_add)|Adds `duration` and `time_point` objects.|  
|[operator< Operator](../vs140/-chrono--operators.md#operator_lt_)|Determines whether one `duration` or `time_point` object is less than another `duration` or `time_point` object.|  
|[operator<= Operator](../vs140/-chrono--operators.md#operator_lt__eq)|Determines whether one `duration` or `time_point` object is less than or equal to another `duration` or `time_point` object.|  
|[operator== Operator](../vs140/-chrono--operators.md#operator_eq_eq)|Determines whether two `duration` objects represent time intervals that have the same length, or whether two `time_point` objects represent the same point in time.|  
|[operator> Operator](../vs140/-chrono--operators.md#operator_gt_)|Determines whether one `duration` or `time_point` object is greater than another `duration` or `time_point` object.|  
|[operator>= Operator](../vs140/-chrono--operators.md#operator_gt__eq)|Determines whether one `duration` or `time_point` object is greater than or equal to another `duration` or `time_point` object.|  
  
### Predefined Duration Types  
 For more information about ratio types that are used in the following typedefs, see [<ratio\>](../vs140/-ratio-.md).  
  
|Typedef|Description|  
|-------------|-----------------|  
|`typedef duration<long long, nano> nanoseconds;`|Synonym for a `duration` type that has a tick period of one nanosecond.|  
|`typedef duration<long long, micro> microseconds;`|Synonym for a `duration` type that has a tick period of one microsecond.|  
|`typedef duration<long long, milli> milliseconds;`|Synonym for a `duration` type that has a tick period of one millisecond.|  
|`typedef duration<long long> seconds;`|Synonym for a `duration` type that has a tick period of one second.|  
|`typedef duration<int, ratio<60> > minutes;`|Synonym for a `duration` type that has a tick period of one minute.|  
|`typedef duration<int, ratio<3600> > hours;`|Synonym for a `duration` type that has a tick period of one hour.|  
  
### Literals  
 **(C++11)**The <chrono\> header defines the following [user-defined literals](../vs140/User-Defined-Literals---C---.md) that you can use for greater convenience, type-safety and maintainability of your code. These literals are defined in the `literals::chrono_literals` inline namespace and are in scope when std::chrono is in scope.  
  
|Literal|Description|  
|-------------|-----------------|  
|chrono::hours operator "" h(unsigned long long Val)|Specifies hours as an integral value.|  
|chrono::duration<double, ratio<3600> > operator "" h(long double Val)|Specifies hours as a floating-point value.|  
|chrono::minutes (operator "" min)(unsigned long long Val)|Specifies minutes as an integral value.|  
|chrono::duration<double, ratio<60> > (operator "" min)( long double Val)|Specifies minutes as a floating-point value.|  
|chrono::seconds operator "" s(unsigned long long Val)|Specifies minutes as an integral value.|  
|chrono::duration<double\> operator "" s(long double Val)|Specifies seconds as a floating-point value.|  
|chrono::milliseconds operator "" ms(unsigned long long Val)|Specifies milliseconds as an integral value.|  
|chrono::duration<double, milli> operator "" ms(long double Val)|Specifies milliseconds as a floating-point value.|  
|chrono::microseconds operator "" us(unsigned long long Val)|Specifies microseconds as an integral value.|  
|chrono::duration<double, micro> operator "" us(long double Val)|Specifies microseconds as a floating-point value.|  
|chrono::nanoseconds operator "" ns(unsigned long long Val)|Specifies nanoseconds as an integral value.|  
|chrono::duration<double, nano> operator "" ns(long double Val)|Specifies nanoseconds as a floating-point value.|  
|||  
  
## Remarks  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)