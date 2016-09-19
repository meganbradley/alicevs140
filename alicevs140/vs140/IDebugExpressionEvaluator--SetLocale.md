---
title: "IDebugExpressionEvaluator::SetLocale"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d3d2027d-74e2-4ae6-bcc7-59d12f873b7c
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpressionEvaluator::SetLocale
This method sets the language to use to create printable results.  
  
## Syntax  
  
```cpp#  
HRESULT SetLocale(   
   WORD wLangID  
);  
```  
  
```c#  
int SetLocale(  
   ushort wLangID  
);  
```  
  
#### Parameters  
 `wLangID`  
 [in] The language identifier.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method may be called many times while the expression evaluator (EE) is loaded, so the EE must be able to switch languages on the fly. The EE uses this locale to return error messages and strings in the appropriate language.  
  
## See Also  
 [IDebugExpressionEvaluator](../vs140/IDebugExpressionEvaluator.md)