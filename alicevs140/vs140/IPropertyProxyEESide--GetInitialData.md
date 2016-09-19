---
title: "IPropertyProxyEESide::GetInitialData"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 36cceb19-2604-4ef9-b42b-5dd30cbe24b1
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IPropertyProxyEESide::GetInitialData
Returns the initial data for this object.  
  
## Syntax  
  
```cpp#  
HRESULT GetInitialData(  
   IEEDataStorage** dataOut  
);  
```  
  
```c#  
int GetInitialData(  
   out IEEDataStorage dataOut  
);  
```  
  
#### Parameters  
 `dataOut`  
 [out] Returns an [IEEDataStorage](../vs140/IEEDataStorage.md) object containing the initial data of this object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IPropertyProxyEESide](../vs140/IPropertyProxyEESide.md)   
 [IEEDataStorage](../vs140/IEEDataStorage.md)