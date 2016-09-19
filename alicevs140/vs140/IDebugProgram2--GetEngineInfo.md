---
title: "IDebugProgram2::GetEngineInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a4f2dc0-e082-4d8d-aeaf-463ab09d279b
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::GetEngineInfo
Gets the name and GUID of the debug engine (DE) running this program.  
  
## Syntax  
  
```cpp#  
HRESULT GetEngineInfo(   
   BSTR* pbstrEngine,  
   GUID* pguidEngine  
);  
```  
  
```c#  
int GetEngineInfo(   
   out string pbstrEngine,  
   out GUID   pguidEngine  
);  
```  
  
#### Parameters  
 `pbstrEngine`  
 [out] Returns the name of the DE running this program.  
  
 `pguidEngine`  
 [out] Returns the GUID of the DE running this program.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Each DE defines its own GUID for identification.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)