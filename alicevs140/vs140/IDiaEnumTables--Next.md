---
title: "IDiaEnumTables::Next"
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
ms.assetid: 8d7bd359-d33e-4317-9674-d89283efd7de
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumTables::Next
Retrieves a specified number of tables in the enumeration sequence.  
  
## Syntax  
  
```cpp#  
HRESULT Next (   
   ULONG       celt,  
   IDiaTable** rgelt,  
   ULONG*      pceltFetched  
);  
```  
  
#### Parameters  
 `celt`  
 [in] The number of tables in the enumerator to be retrieved.  
  
 `rgelt`  
 [out] An array that is to be filled in with the [IDiaTable](../vs140/IDiaTable.md) objects that represent the desired tables.  
  
 `pceltFetched`  
 [out] Returns the number of tables in the fetched enumerator.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if there are no more tables. Otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumTables](../vs140/IDiaEnumTables.md)   
 [IDiaTable](../vs140/IDiaTable.md)