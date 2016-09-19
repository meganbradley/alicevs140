---
title: "Using the Additive Operators"
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
ms.assetid: 7d54841e-436d-4ae8-9865-1ac1829e6f22
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using the Additive Operators
The following examples, which illustrate the addition and subtraction operators, use these declarations:  
  
```  
int i = 4, j;  
float x[10];  
float *px;  
```  
  
 These statements are equivalent:  
  
```  
px = &x[4 + i];  
px = &x[4] + i;    
```  
  
 The value of `i` is multiplied by the length of a **float** and added to `&x[4]`. The resulting pointer value is the address of `x[8]`.  
  
```  
j = &x[i] - &x[i-2];  
```  
  
 In this example, the address of the third element of `x` (given by `x[i–2]`) is subtracted from the address of the fifth element of `x` (given by `x[i]`). The difference is divided by the length of a **float**; the result is the integer value 2.  
  
## See Also  
 [C Additive Operators](../vs140/C-Additive-Operators.md)