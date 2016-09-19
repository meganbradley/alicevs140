---
title: "extent::extent Constructor"
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
ms.assetid: 4b10b446-6f7b-405f-989d-71144b0cc91d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# extent::extent Constructor
Initializes a new instance of the [extent](../vs140/extent-Class--C---AMP-.md) class.  
  
## Syntax  
  
```  
extent() restrict(amp,cpu);  
  
extent(  
   const extent<_Rank>& _Other  
) restrict(amp,cpu);  
  
explicit extent(  
   int _I  
) restrict(amp,cpu);  
  
extent(  
   int _I0,  
   int _I1  
) restrict(amp,cpu);  
  
extent(  
   int _I0,  
   int _I1,  
   int _I2  
) restrict(amp,cpu);  
  
explicit extent(  
   const int _Array[_Rank]  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Array`  
 An array of `_Rank` integers that is used to create the new `extent` object.  
  
 `_I`  
 The length of the extent.  
  
 `_I0`  
 The length of the most significant dimension.  
  
 `_I1`  
 The length of the next-to-most-significant dimension.  
  
 `_I2`  
 The length of the least significant dimension.  
  
 `_Other`  
 An `extent` object on which the new `extent` object is based.  
  
## Remarks  
 The parameterless constructor initializes an `extent` object that has a rank of three.  
  
 If an array is used to construct an `extent` object, the length of the array must match the rank of the `extent` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [extent Structure](../vs140/extent-Class--C---AMP-.md)