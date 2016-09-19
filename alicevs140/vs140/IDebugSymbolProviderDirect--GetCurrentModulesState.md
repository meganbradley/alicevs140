---
title: "IDebugSymbolProviderDirect::GetCurrentModulesState"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a0c85318-5686-4eed-b213-21f2b9e681e6
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSymbolProviderDirect::GetCurrentModulesState
Retrieves information about the symbol group of which the symbol provider is a member.  
  
## Syntax  
  
```cpp#  
HRESULT GetCurrentModulesState(  
    DWORD*          pState,  
    unsigned long * count  
);  
```  
  
```c#  
int GetCurrentModulesState(  
    out uint pState,  
    out uint count  
);  
```  
  
#### Parameters  
 `pState`  
 [out] The state of the symbol provider group.  
  
 `count`  
 [out] Number of modules in the group.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The state is changed whenever a module is added to, or removed from, the symbol group. Therefore, this method can be used to detect if a symbol group has been modified.  
  
## See Also  
 [IDebugSymbolProviderDirect](../vs140/IDebugSymbolProviderDirect.md)