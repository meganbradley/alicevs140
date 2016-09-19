---
title: "IDebugSettingsCallback2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e525d0b-7d7a-4d1c-8b78-e1398fa922f2
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSettingsCallback2
Enables debug engines to read metric settings remotely.  
  
## Syntax  
  
```  
IDebugSettingsCallback2D : IUnknown  
```  
  
## Notes for Implementers  
 This interface is implemented by the event callback of the session debug manager and consumed by debug engines. It could also be used locally instead of Dbgmetric[d].lib.  
  
## Methods  
 The following table shows the methods of `IDebugSettingsCallback2`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugSettingsCallback2::EnumEEs](../vs140/IDebugSettingsCallback2--EnumEEs.md)|Enumerates the available expression evaluators given the language and vendor identifiers.|  
|[IDebugSettingsCallback2::GetEELocalObject](../vs140/IDebugSettingsCallback2--GetEELocalObject.md)|Retrieves a expression evaluator local object given the metric.|  
|[IDebugSettingsCallback2::GetEEMetricDword](../vs140/IDebugSettingsCallback2--GetEEMetricDword.md)|Retrieves a value that corresponds to the specified metric of the expression evaluator.|  
|[IDebugSettingsCallback2::GetEEMetricFile](../vs140/IDebugSettingsCallback2--GetEEMetricFile.md)|Retrieves the expression evaluator metric file given the name or the metric.|  
|[IDebugSettingsCallback2::GetEEMetricGuid](../vs140/IDebugSettingsCallback2--GetEEMetricGuid.md)|Retrieves the unique identifier for a expression evaluator metric given its name.|  
|[IDebugSettingsCallback2::GetEEMetricString](../vs140/IDebugSettingsCallback2--GetEEMetricString.md)|Retrieves the value string of an expression evaluator metric given its name.|  
|[IDebugSettingsCallback2::GetMetricDword](../vs140/IDebugSettingsCallback2--GetMetricDword.md)|Retrieves the value of a metric given its name.|  
|[IDebugSettingsCallback2::GetMetricGuid](../vs140/IDebugSettingsCallback2--GetMetricGuid.md)|Retrieves the unique identifier of a metric given its name.|  
|[IDebugSettingsCallback2::GetMetricString](../vs140/IDebugSettingsCallback2--GetMetricString.md)|Retrieves the value string of the metric given its name.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## Example  
 The following example shows a function that takes an **IDebugSettingsCallback2** object as a parameter.  
  
```cpp#  
HRESULT GetDebugSettingsCallback (IDebugSettingsCallback2 **ppCallback)  
{  
    HRESULT hRes = E_FAIL;  
  
    if ( ppCallback )  
   {  
        if ( EVAL(m_pdec) )  
            hRes = m_pdec->QueryInterface(IID_IDebugSettingsCallback2, (void **)ppCallback);  
        else  
            hRes = E_FAIL;  
    }  
    else  
        hRes = E_INVALIDARG;  
  
    return ( hRes );  
}  
```