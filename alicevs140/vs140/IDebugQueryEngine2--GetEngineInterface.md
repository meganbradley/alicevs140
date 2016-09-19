---
title: "IDebugQueryEngine2::GetEngineInterface"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ed84aa98-7ec7-48f3-97ae-821090bc3664
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugQueryEngine2::GetEngineInterface
Gets a custom debug engine (DE) interface.  
  
## Syntax  
  
```cpp#  
HRESULT GetEngineInterface(   
   IUnknown** ppUnk  
);  
```  
  
```c#  
int GetEngineInterface(   
   out object ppUnk  
);  
```  
  
#### Parameters  
 `ppUnk`  
 [out] Returns an `IUnknown` object represents the debug engine (DE), and which can be queried for any other valid interface associated with a DE (for example [IDebugEngine2](../vs140/IDebugEngine2.md) or [IDebugEngineLaunch2](../vs140/IDebugEngineLaunch2.md)).  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The resulting interface should be used with care because calling through interfaces retrieved from this method circumvents the session debug manager's processing and may result in the SDM getting into a bad state or generating errors while debugging.  
  
## See Also  
 [IDebugQueryEngine2](../vs140/IDebugQueryEngine2.md)   
 [IDebugEngine2](../vs140/IDebugEngine2.md)   
 [IDebugEngineLaunch2](../vs140/IDebugEngineLaunch2.md)