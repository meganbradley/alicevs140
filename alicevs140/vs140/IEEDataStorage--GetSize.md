---
title: "IEEDataStorage::GetSize"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 33d232c4-1239-4abc-922b-e1bc5b908169
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEEDataStorage::GetSize
Returns the number of bytes contained in this object.  
  
## Syntax  
  
```cpp#  
HRESULT GetSize(  
   ULONG* size  
);  
```  
  
```c#  
int GetSize(  
   out uint size  
);  
```  
  
#### Parameters  
 `size`  
 [out] The number of bytes contained in this object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Use the [IEEDataStorage::GetData](../vs140/IEEDataStorage--GetData.md) method to retrieve the actual data bytes.  
  
## See Also  
 [IEEDataStorage](../vs140/IEEDataStorage.md)   
 [IEEDataStorage::GetData](../vs140/IEEDataStorage--GetData.md)