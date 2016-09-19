---
title: "IDebugProcess2::Attach"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40d78417-fde2-45c3-96c9-16e06bd9008d
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::Attach
Attaches the session debug manager (SDM) to the process.  
  
## Syntax  
  
```cpp#  
HRESULT Attach(   
   IDebugEventCallback2* pCallback,  
   GUID*                 rgguidSpecificEngines,  
   DWORD                 celtSpecificEngines,  
   HRESULT*              rghrEngineAttach  
);  
```  
  
```c#  
int Attach(   
   IDebugEventCallback2 pCallback,  
   Guid[]               rgguidSpecificEngines,  
   uint                 celtSpecificEngines,  
   int[]                rghrEngineAttach  
);  
```  
  
#### Parameters  
 `pCallback`  
 [in] An [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) object that is used for debug event notification.  
  
 `rgguidSpecificEngines`  
 [in] An array of GUIDs of debug engines to be used to debug programs running in the process. This parameter can be a null value. See Remarks for details.  
  
 `celtSpecificEngines`  
 [in] The number of debug engines in the `rgguidSpecificEngines` array and the size of the `rghrEngineAttach` array.  
  
 `rghrEngineAttach`  
 [in, out] An array of HRESULT codes returned by the debug engines. The size of this array is specified in the `celtSpecificEngines` parameter. Each code is typically either `S_OK` or `S_ATTACH_DEFERRED`. The latter indicates that the DE is currently attached to no programs.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The following table shows other possible values.  
  
|Value|Description|  
|-----------|-----------------|  
|`E_ATTACH_DEBUGGER_ALREADY_ATTACHED`|The specified process is already attached to the debugger.|  
|`E_ATTACH_DEBUGGEE_PROCESS_SECURITY_VIOLATION`|A security violation occurred during the attach procedure.|  
|`E_ATTACH_CANNOT_ATTACH_TO_DESKTOP`|A desktop process cannot be attached to the debugger.|  
  
## Remarks  
 Attaching to a process attaches the SDM to all programs running in that process that can be debugged by the debug engines (DE) specified in the `rgguidSpecificEngines` array. Set the `rgguidSpecificEngines` parameter to a null value or include `GUID_NULL` in the array to attach to all programs in the process.  
  
 All debug events that occur in the process are sent to the given [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) object. This `IDebugEventCallback2` object is provided when the SDM calls this method.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)