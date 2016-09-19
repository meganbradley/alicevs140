---
title: "IDebugSettingsCallback2::GetEEMetricDword"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c5f8f417-0ef0-4fd0-a779-b0a8ead4effe
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSettingsCallback2::GetEEMetricDword
Retrieves a value that corresponds to the specified metric of the expression evaluator.  
  
## Syntax  
  
```cpp#  
HRESULT GetEEMetricDword(  
   REFGUID guidLang,  
   REFGUID guidVendor,  
   LPCWSTR pszMetric,  
   DWORD*  pdwValue  
);  
```  
  
```c#  
private int GetEEMetricDword(  
   ref Guid guidLang,  
   ref Guid guidVendor,  
   string   pszMetric,  
   out uint pdwValue  
);  
```  
  
#### Parameters  
 `guidLang`  
 [in] Unique identifier of the programming language.  
  
 `guidVendor`  
 [in] Unique identifier of the vendor.  
  
 `pszMetric`  
 [in] Name of the metric.  
  
 `pdwValue`  
 [out] Returns the value that corresponds to the metric string.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugSettingsCallback2](../vs140/IDebugSettingsCallback2.md)