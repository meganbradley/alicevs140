---
title: "IDiaPropertyStorage::ReadDWORD"
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
ms.assetid: 5f4c034e-a9d3-4560-94b5-ede524741439
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaPropertyStorage::ReadDWORD
Reads `DWORD` values in a property set.  
  
## Syntax  
  
```cpp#  
HRESULT ReadDWORD (   
   PROPID id,  
   DWORD* pValue  
);  
```  
  
#### Parameters  
 `id`  
 [in] Identifier of the property to be read (`PROPID` is defined in WTypes.h as a `ULONG`).  
  
 `pValue`  
 [out] Returns the property value.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns an error code. Returns `E_INVALIDARG` if the property is not of type `DWORD`.  
  
## Remarks  
 A `DWORD` is defined by Windows as a 32-bit unsigned integer.  
  
## See Also  
 [IDiaPropertyStorage](../vs140/IDiaPropertyStorage.md)