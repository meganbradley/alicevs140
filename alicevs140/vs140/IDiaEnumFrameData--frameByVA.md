---
title: "IDiaEnumFrameData::frameByVA"
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
ms.assetid: 0b1e441b-710a-46d8-8060-bed39071c834
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumFrameData::frameByVA
Returns a frame by virtual address (VA).  
  
## Syntax  
  
```cpp#  
HRESULT frameByVA(   
   ULONGLONG       virtualAddress,  
   IDiaFrameData** frame  
);  
```  
  
#### Parameters  
 virtualAddress  
 [in] VA of the frame of interest.  
  
 frame  
 [out] Returns an [IDiaFrameData](../vs140/IDiaFrameData.md) object that represents the frame that contains the address provided.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if no frame data matches the specified address. Otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumFrameData](../vs140/IDiaEnumFrameData.md)   
 [IDiaFrameData](../vs140/IDiaFrameData.md)