---
title: "Math Error Constants"
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
ms.assetid: 4be933a6-674e-45a5-8ac9-090023542f5b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Math Error Constants
## Syntax  
  
```  
  
#include <math.h>  
  
```  
  
## Remarks  
 The math routines of the run-time library can generate math error constants.  
  
 These errors, described as follows, correspond to the exception types defined in MATH.H and are returned by the `_matherr` function when a math error occurs.  
  
|Constant|Meaning|  
|--------------|-------------|  
|`_DOMAIN`|Argument to function is outside domain of function.|  
|`_OVERFLOW`|Result is too large to be represented in function's return type.|  
|`_PLOSS`|Partial loss of significance occurred.|  
|`_SING`|Argument singularity: argument to function has illegal value. (For example, value 0 is passed to function that requires nonzero value.)|  
|`_TLOSS`|Total loss of significance occurred.|  
|`_UNDERFLOW`|Result is too small to be represented.|  
  
## See Also  
 [_matherr](../vs140/_matherr.md)   
 [Global Constants](../vs140/Global-Constants.md)