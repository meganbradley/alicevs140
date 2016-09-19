---
title: "IDebugProgram2::EnumModules"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 876ac9da-3b7c-4156-b79a-8f340e9fcea6
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::EnumModules
Retrieves a list of the modules that this program has loaded and is executing.  
  
## Syntax  
  
```cpp#  
HRESULT EnumModules(   
   IEnumDebugModules2** ppEnum  
);  
```  
  
```c#  
int EnumModules(   
   out IEnumDebugModules2 ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns an [IEnumDebugModules2](../vs140/IEnumDebugModules2.md) object that contains a list of the modules.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 A module is a DLL or assembly and is typically listed in the **Modules** debug window.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IEnumDebugModules2](../vs140/IEnumDebugModules2.md)