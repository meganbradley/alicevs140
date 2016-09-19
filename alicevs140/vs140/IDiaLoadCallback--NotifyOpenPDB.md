---
title: "IDiaLoadCallback::NotifyOpenPDB"
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
ms.assetid: c0547f99-8468-4e57-82ca-9ef7d6707c8a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaLoadCallback::NotifyOpenPDB
Called when a candidate .pdb file is opened.  
  
## Syntax  
  
```cpp#  
HRESULT NotifyOpenPDB (   
   LPCOLESTR pdbPath,  
   HRESULT   resultCode  
);  
```  
  
#### Parameters  
 `pdbPath`  
 [in] The full path of the .pdb file.  
  
 `resultCode`  
 [in] Code that indicates the success (`S_OK`) or failure of the load as applied to this file.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The return code is typically ignored.  
  
## See Also  
 [IDiaLoadCallback2](../vs140/IDiaLoadCallback2.md)