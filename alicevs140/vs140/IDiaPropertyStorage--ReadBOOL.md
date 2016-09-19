---
title: "IDiaPropertyStorage::ReadBOOL"
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
ms.assetid: ad1822db-4572-48f7-9919-f8137f6701f2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaPropertyStorage::ReadBOOL
Reads `BOOL` values in a property set.  
  
## Syntax  
  
```cpp#  
HRESULT ReadBOOL (   
   PROPID id,  
   BOOL*  pValue  
);  
```  
  
#### Parameters  
 `id`  
 [in] Identifier of the property to be read (`PROPID` is defined in WTypes.h as a `ULONG`).  
  
 `pValue`  
 [out] Returns the property value.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns an error code. Returns `E_INVALIDARG` if the property is not of type `BOOL`.  
  
## Remarks  
 For consistent results, interpret the `BOOL` value so that nonzero values are `TRUE` and zero is `FALSE`.  
  
## See Also  
 [IDiaPropertyStorage](../vs140/IDiaPropertyStorage.md)