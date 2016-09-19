---
title: "IDiaTable::get__NewEnum"
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
ms.assetid: ee89bba8-5d5c-4a0b-aa0d-1aad56baa380
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaTable::get__NewEnum
Retrieves the <xref:System.Runtime.InteropServices.ComTypes.IEnumVARIANT?qualifyHint=False> version of this enumerator.  
  
## Syntax  
  
```cpp#  
HRESULT get__NewEnum (   
   IUnknown** pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the `IUnknown` interface that represents the <xref:System.Runtime.InteropServices.ComTypes.IEnumVARIANT?qualifyHint=False> version of this enumerator.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaTable](../vs140/IDiaTable.md)