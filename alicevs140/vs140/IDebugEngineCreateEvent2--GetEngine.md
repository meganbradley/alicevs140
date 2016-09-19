---
title: "IDebugEngineCreateEvent2::GetEngine"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 187d24ed-9f9a-4418-a0ef-b8a19f54652c
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngineCreateEvent2::GetEngine
Retrieves the object that represents the newly created debug engine (DE).  
  
## Syntax  
  
```cpp#  
HRESULT GetEngine(   
   IDebugEngine2** pEngine  
);  
```  
  
```c#  
int GetEngine(   
   out IDebugEngine2 pEngine  
);  
```  
  
#### Parameters  
 `pEngine`  
 [out] Returns an [IDebugEngine2](../vs140/IDebugEngine2.md) object that represents the newly created DE.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugEngineCreateEvent2](../vs140/IDebugEngineCreateEvent2.md)   
 [IDebugEngine2](../vs140/IDebugEngine2.md)