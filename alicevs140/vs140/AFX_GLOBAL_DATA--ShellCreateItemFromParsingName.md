---
title: "AFX_GLOBAL_DATA::ShellCreateItemFromParsingName"
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
ms.assetid: ecb61b6d-8a96-4e2c-aa17-c7ad8eea297d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::ShellCreateItemFromParsingName
Creates and initializes a Shell item object from a parsing name.  
  
## Syntax  
  
```  
HRESULT ShellCreateItemFromParsingName(  
   PCWSTR pszPath,  
   IBindCtx *pbc,  
   REFIID riid,  
   void **ppv  
);  
```  
  
#### Parameters  
 `pszPath`  
 [in] A pointer to a display name.  
  
 `pbc`  
 A pointer to a bind context that controls the parsing operation.  
  
 `riid`  
 A reference to an interface ID.  
  
 `ppv`  
 [out] When this function returns, contains the interface pointer requested in `riid`. This will typically be `IShellItem` or `IShellItem2`.  
  
## Return Value  
 Returns S_OK if successful; an error value otherwise.  
  
## Remarks  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)