---
title: "IDiaEnumTables::get_Count"
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
ms.assetid: 30fa316b-a746-4028-acae-4efcd2066f38
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumTables::get_Count
Retrieves the number of tables.  
  
## Syntax  
  
```cpp#  
HRESULT get_Count (    LONG* pRetVal  
);  
  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the number of tables.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumTables](../vs140/IDiaEnumTables.md)   
 [IDiaEnumTables::Item](../vs140/IDiaEnumTables--Item.md)