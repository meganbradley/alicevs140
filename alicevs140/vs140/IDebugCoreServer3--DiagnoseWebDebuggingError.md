---
title: "IDebugCoreServer3::DiagnoseWebDebuggingError"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8c4570ca-ae55-42f2-bbaa-8d8e75d2fa19
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer3::DiagnoseWebDebuggingError
Attempts to determine why an auto-attach failed.  
  
## Syntax  
  
```cpp#  
HRESULT DiagnoseWebDebuggingError(  
   LPCWSTR pszUrl  
);  
```  
  
```c#  
int DiagnoseWebDebuggingError(  
   string pszUrl  
);  
```  
  
#### Parameters  
 `pszUrl`  
 [in] Not currently used; should always be set to a null value.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The following are other typical return codes:  
  
|Code|Description|  
|----------|-----------------|  
|`S_WEBDBG_UNABLE_TO_DIAGNOSE`|Cannot determine why the remote server failed to start debugging.|  
|`S_WEBDBG_DEBUG_VERB_BLOCKED`|Cannot debug on remote server, possibly due to insufficient permissions or because the DEBUG verb is not enabled.|  
|`E_WEBDBG_DEBUG_VERB_BLOCKED`|The web server has been locked down and is blocking the DEBUG verb, which is required to enable debugging.|  
  
## See Also  
 [IDebugCoreServer3](../vs140/IDebugCoreServer3.md)