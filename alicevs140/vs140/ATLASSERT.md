---
title: "ATLASSERT"
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
ms.topic: reference
ms.assetid: 98e3e0fc-77e2-499b-a6f6-b17a21c6fbd3
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLASSERT
The `ATLASSERT` macro performs the same functionality as the [_ASSERTE](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) macro found in the C run-time library.  
  
## Syntax  
  
```  
  
ATLASSERT( booleanExpression );  
```  
  
#### Parameters  
 `booleanExpression`  
 Expression (including pointers) that evaluates to nonzero or 0.  
  
## Remarks  
 In debug builds, `ATLASSERT` evaluates `booleanExpression` and generates a debug report when the result is false.  
  
## Requirements  
 **Header:** atldef.h  
  
## See Also  
 [Debugging and Error Reporting Macros](../vs140/Debugging-and-Error-Reporting-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)