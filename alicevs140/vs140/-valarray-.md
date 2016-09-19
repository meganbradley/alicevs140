---
title: "&lt;valarray&gt;"
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
ms.assetid: 30835415-21c1-4801-8f24-6bbef7dd8ecd
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;valarray&gt;
Defines the template class valarray and numerous supporting template classes and functions.  
  
## Syntax  
  
```  
#include <valarray>  
  
```  
  
## Remarks  
 These template classes and functions are permitted unusual latitude in the interest of improved performance. Specifically, any function returning type **valarray<**T1**>** may return an object of some other type T2. In that case, any function that accepts one or more arguments of type **valarray<**T2**>** must have overloads that accept arbitrary combinations of those arguments, each replaced with an argument of type T2.  
  
### Functions  
  
|||  
|-|-|  
|[abs](../vs140/-valarray--functions.md#abs)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the absolute value of the elements of the input valarray.|  
|[acos](../vs140/-valarray--functions.md#acos)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the arccosine of the elements of the input valarray.|  
|[asin](../vs140/-valarray--functions.md#asin)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the arcsine of the elements of the input valarray.|  
|[atan](../vs140/-valarray--functions.md#atan)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the principal value of the arctangent of the elements of the input valarray.|  
|[atan2](../vs140/-valarray--functions.md#atan2)|Returns a valarray whose elements are equal to the arctangent of the Cartesian components specified by a combination of constants and elements of valarrays.|  
|[cos](../vs140/-valarray--functions.md#cos)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the cosine of the elements of the input valarray.|  
|[cosh](../vs140/-valarray--functions.md#cosh)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the hyperbolic cosine of the elements of the input valarray.|  
|[exp](../vs140/-valarray--functions.md#exp)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the natural exponential of the elements of the input valarray.|  
|[log](../vs140/-valarray--functions.md#log)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the natural logarithm of the elements of the input valarray.|  
|[log10](../vs140/-valarray--functions.md#log10)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the base 10 or common logarithm of the elements of the input valarray.|  
|[pow](../vs140/-valarray--functions.md#pow)|Operates on the elements of input valarrays and constants, returning a valarray whose elements are equal to a base specified either by the elements of an input valarray or a constant raised to an exponent specified either by the elements of an input valarray or a constant.|  
|[sin](../vs140/-valarray--functions.md#sin)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the sine of the elements of the input valarray.|  
|[sinh](../vs140/-valarray--functions.md#sinh)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the hyperbolic sine of the elements of the input valarray.|  
|[sqrt](../vs140/-valarray--functions.md#sqrt)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the square root of the elements of the input valarray.|  
|[swap](../vs140/-valarray--functions.md#swap)||  
|[tan](../vs140/-valarray--functions.md#tan)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the tangent of the elements of the input valarray.|  
|[tanh](../vs140/-valarray--functions.md#tanh)|Operates on the elements of an input valarray, returning a valarray whose elements are equal to the hyperbolic tangent of the elements of the input valarray.|  
  
### Operators  
  
|||  
|-|-|  
|[operator!=](../vs140/-valarray--operators.md#operator_neq)|Tests whether the corresponding elements of two equally sized valarrays are unequal or whether all the elements of a valarray are unequal a specified value of the valarray's element type.|  
|[operator%](../vs140/-valarray--operators.md#operator_mod)|Obtains the remainder of dividing the corresponding elements of two equally sized valarrays or of dividing a valarray by a specified value of the valarray's element type or of dividing a specified value by a valarray.|  
|[operator&](../vs140/-valarray--operators.md#operator_amp_)|Obtains the bitwise **AND** between corresponding elements of two equally sized valarrays or between a valarray and a specified value of the element type.|  
|[operator&&](../vs140/-valarray--operators.md#operator_amp__amp_)|Obtains the logical **AND** between corresponding elements of two equally sized valarrays or between a valarray and a specified value of the valarray's element type.|  
|[operator>](../vs140/-valarray--operators.md#operator_gt_)|Tests whether the elements of one valarray are greater than the elements of an equally sized valarray or whether all the elements of a valarray are greater or less than a specified value of the valarray's element type.|  
|[operator>=](../vs140/-valarray--operators.md#operator_gt__eq)|Tests whether the elements of one valarray are greater than or equal to the elements of an equally sized valarray or whether all the elements of a valarray are greater than or equal to or less than or equal to a specified value.|  
|[operator>>](../vs140/-valarray--operators.md#operator_gt__gt_)|Right-shifts the bits for each element of a valarray a specified number of positions or by an element-wise amount specified by a second valarray.|  
|[operator<](../vs140/-valarray--operators.md#operator_lt_)|Tests whether the elements of one valarray are less than the elements of an equally sized valarray or whether all the elements of a valarray are greater or less than a specified value.|  
|[operator<=](../vs140/-valarray--operators.md#operator_lt__eq)|Tests whether the elements of one valarray are less than or equal to the elements of an equally sized valarray or whether all the elements of a valarray are greater than or equal to or less than or equal to a specified value.|  
|[operator<<](../vs140/-valarray--operators.md#operator_lt__lt_)|Left shifts the bits for each element of a valarray a specified number of positions or by an element-wise amount specified by a second valarray.|  
|[operator*](../vs140/-valarray--operators.md#operator_star)|Obtains the element-wise product between corresponding elements of two equally sized valarrays or of between a valarray a specified value of the valarray's element type.|  
|[operator+](../vs140/-valarray--operators.md#operator_add)|Obtains the element-wise sum between corresponding elements of two equally sized valarrays or of between a valarray a specified value of the valarray's element type.|  
|[operator-](../vs140/-valarray--operators.md#operator-)|Obtains the element-wise difference between corresponding elements of two equally sized valarrays or of between a valarray a specified value of the valarray's element type.|  
|[operator/](../vs140/-valarray--operators.md#operator_)|Obtains the element-wise quotient between corresponding elements of two equally sized valarrays or of between a valarray a specified value of the valarray's element type.|  
|[operator==](../vs140/-valarray--operators.md#operator_eq_eq)|Tests whether the corresponding elements of two equally sized valarrays are equal or whether all the elements of a valarray are equal a specified value of the valarray's element type.|  
|[operator^](../vs140/-valarray--operators.md#operator_xor)|Obtains the bitwise exclusive `OR` between corresponding elements of two equally sized valarrays or between a valarray and a specified value of the element type.|  
|[operator&#124;](../vs140/-valarray--operators.md#operator_or)|Obtains the bitwise `OR` between corresponding elements of two equally sized valarrays or between a valarray and a specified value of the element type.|  
|[operator&#124;&#124;](../vs140/-valarray--operators.md#operator_lor)|Obtains the logical `OR` between corresponding elements of two equally sized valarrays or between a valarray and a specified value of the valarray's element type.|  
  
### Classes  
  
|||  
|-|-|  
|[gslice Class](../vs140/gslice-Class.md)|A utility class to valarray that is used to define multi-dimensional slices of a valarray.|  
|[gslice_array Class](../vs140/gslice_array-Class.md)|An internal, auxiliary template class that supports general slice objects by providing operations between subset arrays defined by the general slice of a valarray.|  
|[indirect_array Class](../vs140/indirect_array-Class.md)|An internal, auxiliary template class that supports objects that are subsets of valarrays by providing operations between subset arrays defined by specifying a subset of indices of a parent valarray.|  
|[mask_array Class](../vs140/mask_array-Class.md)|An internal, auxiliary template class that supports objects that are subsets of parent valarrays, specified with a Boolean expression, by providing operations between the subset arrays.|  
|[slice Class](../vs140/slice-Class.md)|A utility class to valarray that is used to define one-dimensional, vector-like subsets of a valarray.|  
|[slice_array Class](../vs140/slice_array-Class.md)|An internal, auxiliary template class that supports slice objects by providing operations between subset arrays defined by the slice of a valarray.|  
|[valarray Class](../vs140/valarray-Class.md)|The template class describes an object that controls a sequence of elements of type **Type** that are stored as an array and designed for performing high-speed mathematical operations, optimized for computational performance.|  
  
### Specializations  
  
|||  
|-|-|  
|[valarray<bool\> Class](../vs140/valarray-bool--Class.md)|A specialized version of the template class valarray<**Type**> to elements of type `bool`.|  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)