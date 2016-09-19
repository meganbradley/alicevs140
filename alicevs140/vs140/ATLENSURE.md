---
title: "ATLENSURE"
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
ms.assetid: 41d47432-5e73-432e-8ab7-acaf8fde3ffb
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLENSURE
This macro is used to validate parameters passed to a function.  
  
## Syntax  
  
```  
  
      ATLENSURE(  
      booleanExpression  
      );  
ATLENSURE_THROW(booleanExpression, hr);  
```  
  
#### Parameters  
 `booleanExpression`  
 Specifies a boolean expression to be tested.  
  
 `hr`  
 Specifies an error code to return.  
  
## Remarks  
 These macros provide a mechanism to detect and notify the user of incorrect parameter usage.  
  
 The macro calls `ATLASSERT` and if the condition fails calls `AtlThrow`.  
  
 In the **ATLENSURE** case, `AtlThrow` is called with E_FAIL.  
  
 In the **ATLENSURE_THROW** case, `AtlThrow` is called with the specified HRESULT.  
  
 The difference between **ATLENSURE** and `ATLASSERT` is that **ATLENSURE** throws an exception in Release builds as well as in Debug builds.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#108](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#108)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Debugging and Error Reporting Macros](../vs140/Debugging-and-Error-Reporting-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [ATLASSERT](../vs140/ATLASSERT.md)   
 [ENSURE (MFC)](../vs140/ENSURE--MFC-.md)