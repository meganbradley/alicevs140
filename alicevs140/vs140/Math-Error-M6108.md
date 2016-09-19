---
title: "Math Error M6108"
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
ms.topic: error-reference
ms.assetid: 054893b4-49bc-45d9-882f-7cb50ba387c0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Math Error M6108
square root  
  
 The operand in a square-root operation was negative.  
  
 Program terminates with exit code 136.  
  
> [!NOTE]
>  The `sqrt` function in the C run-time library and the FORTRAN intrinsic function **SQRT** do not generate this error. The C `sqrt` function checks the argument before performing the operation and returns an error value if the operand is negative. The FORTRAN **SQRT** function generates the DOMAIN error [M6201](../vs140/Math-Error-M6201.md) instead of this error.