---
title: "IDiaEnumDebugStreamData::Clone"
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
ms.assetid: e7f17750-0694-4634-bf34-c821cd265c2f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumDebugStreamData::Clone
Creates an enumerator that contains the same enumerated sequence as the current enumerator.  
  
## Syntax  
  
```cpp#  
HRESULT Clone (   
   IDiaEnumDebugStreamData** ppenum  
);  
```  
  
#### Parameters  
 ppenum  
 [out] Returns an [IDiaEnumDebugStreamData](../vs140/IDiaEnumDebugStreamData.md) object that contains the duplicated sequence of debug data stream records.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumDebugStreamData](../vs140/IDiaEnumDebugStreamData.md)