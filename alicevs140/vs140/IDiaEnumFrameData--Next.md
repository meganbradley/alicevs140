---
title: "IDiaEnumFrameData::Next"
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
ms.assetid: 546e2e23-efb2-425a-96a1-808c67c519fb
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumFrameData::Next
Retrieves a specified number of frame data elements in the enumeration sequence.  
  
## Syntax  
  
```cpp#  
HRESULT Next (   
   ULONG           celt,   
   IDiaFrameData** rgelt,  
   ULONG*          pceltFetched  
);  
```  
  
#### Parameters  
 celt  
 [in] The number of frame data elements in the enumerator to be retrieved.  
  
 rgelt  
 [out] An array of [IDiaFrameData](../vs140/IDiaFrameData.md) objects to be filled in with the requested frame data elements.  
  
 pceltFetched  
 [out] Returns the number of frame data elements in the fetched enumerator.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if there are no more records. Otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumFrameData](../vs140/IDiaEnumFrameData.md)   
 [IDiaFrameData](../vs140/IDiaFrameData.md)