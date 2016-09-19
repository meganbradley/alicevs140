---
title: "IDebugExpressionEvaluator::SetRegistryRoot"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 790886d8-1975-4d3c-9a75-cd86c1faf4ca
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpressionEvaluator::SetRegistryRoot
This method sets the registry root. Used for side-by-side debugging.  
  
## Syntax  
  
```cpp#  
HRESULT SetRegistryRoot (   
   LPCOLESTR ustrRegistryRoot  
);  
```  
  
```c#  
int SetRegistryRoot(  
   string ustrRegistryRoot  
);  
```  
  
#### Parameters  
 `ustrRegistryRoot`  
 [in] The new registry root.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The specified registry root is typically set when the expression evaluator is first instantiated and points to the registry key for a specific version of Visual Studio (HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio\\*X.Y*, where *X.Y* is a version number).  
  
## See Also  
 [IDebugExpressionEvaluator](../vs140/IDebugExpressionEvaluator.md)