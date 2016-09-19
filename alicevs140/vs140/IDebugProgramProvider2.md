---
title: "IDebugProgramProvider2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a9ec7b3e-a59c-4069-b2ee-6f45916eeb78
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramProvider2
This registered interface allows the session debug manager (SDM) to obtain information about programs that have been "published" through the [IDebugProgramPublisher2](../vs140/IDebugProgramPublisher2.md) interface.  
  
## Syntax  
  
```  
IDebugProgramProvider2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to provide information about programs being debugged. This interface is registered in the DE section of the registry using the metric `metricProgramProvider`, as described in [Debugging SDK Helpers](../vs140/SDK-Helpers-for-Debugging.md).  
  
## Notes for Callers  
 Call COM's `CoCreateInstance` function with the `CLSID` of the program provider that is obtained from the registry. See the Example.  
  
## Methods in Vtable order  
  
|Method|Description|  
|------------|-----------------|  
|[GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md)|Obtains information about programs running, filtered in a variety of ways.|  
|[GetProviderProgramNode](../vs140/IDebugProgramProvider2--GetProviderProgramNode.md)|Gets a program node, given a specific process ID.|  
|[WatchForProviderEvents](../vs140/IDebugProgramProvider2--WatchForProviderEvents.md)|Establishes a callback to watch for provider events associated with specific kinds of processes.|  
|[IDebugProgramProvider2::SetLocale](../vs140/IDebugProgramProvider2--SetLocale.md)|Establishes a locale for any language-specific resources needed by the DE.|  
  
## Remarks  
 Normally, a process uses this interface to find out about the programs running in that process.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## Example  
  
```cpp#  
IDebugProgramProvider2 *GetProgramProvider(GUID *pDebugEngineGuid)  
{  
    // This is typically defined globally.  For this example, it is  
    // defined here.  
    static const WCHAR strRegistrationRoot[] = L"Software\\Microsoft\\VisualStudio\\8.0Exp";  
    IDebugProgramProvider2 *pProvider = NULL;  
    if (pDebugEngineGuid != NULL) {  
        CLSID clsidProvider = { 0 };  
        ::GetMetric(NULL,  
                    metrictypeEngine,  
                    *pDebugEngineGuid,  
                    metricProgramProvider,  
                    &clsidProvider,  
                    strRegistrationRoot);  
        if (!IsEqualGUID(clsidProvider,GUID_NULL)) {  
            CComPtr<IDebugProgramProvider2> spProgramProvider;  
            spProgramProvider.CoCreateInstance(clsidProvider);  
            if (spProgramProvider != NULL) {  
                pProvider = spProgramProvider.Detach();  
            }  
        }  
    }  
    return(pProvider);  
}  
```  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProgramPublisher2](../vs140/IDebugProgramPublisher2.md)   
 [Debugging SDK Helpers](../vs140/SDK-Helpers-for-Debugging.md)