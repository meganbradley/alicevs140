---
title: "IDiaPropertyStorage::ReadPropertyNames"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f8bcab77-afca-4a8f-8710-697842f8a518
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaPropertyStorage::ReadPropertyNames
Retrieves corresponding string names for given property identifiers.  
  
## Syntax  
  
```cpp  
HRESULT ReadPropertyNames (  
   ULONG         cpropid,  
   PROPID const* rgpropid,  
   BSTR*         rglpwstrName  
);  
```  
  
#### Parameters  
 `cpropid`  
 [in] Number of property ids in `rgpropid`.  
  
 `rgpropid`  
 [in] Array of property ids for which to get the names (`PROPID` is defined in WTypes.h as a `ULONG`).  
  
 `rglpwstrName`  
 [in, out] Array of property names for the specified property ids. The array must be pre-allocated to hold the requested number of property names and must be able to hold at least `cpropid``BSTR` strings.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns an error code.  
  
## Remarks  
 The returned property names must be freed (by calling the `SysFreeString` function) when they are no longer needed.  
  
## See Also  
 [IDiaPropertyStorage](../vs140/IDiaPropertyStorage.md)