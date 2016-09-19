---
title: "IDiaStackWalkHelper::imageForVA"
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
ms.assetid: 8d4edabf-3c01-4fef-8b61-4779f3371067
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackWalkHelper::imageForVA
Returns the start of an executable's image in memory given a virtual address somewhere in the executable's memory space.  
  
## Syntax  
  
```cpp#  
HRESULT imageForVA(  
   ULONGLONG  vaContext,  
   ULONGLONG *pvaImageStart  
);  
```  
  
#### Parameters  
 `vaContext`  
 [in] The virtual address that lies somewhere in the executable's space.  
  
 `pvaImageStart`  
 [out] Returns the starting virtual address of the executable's image.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaStackWalkHelper](../vs140/IDiaStackWalkHelper.md)