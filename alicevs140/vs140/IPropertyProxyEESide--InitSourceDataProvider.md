---
title: "IPropertyProxyEESide::InitSourceDataProvider"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5156f593-5052-4e3a-9d02-081916fb342d
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IPropertyProxyEESide::InitSourceDataProvider
Initializes the source data for this object and returns an object containing the initial data.  
  
## Syntax  
  
```cpp#  
HRESULT InitSourceDataProvider(  
   IEEDataStorage** dataOut  
);  
```  
  
```c#  
int InitSourceDataProvider(  
   out IEEDataStorage dataOut  
);  
```  
  
#### Parameters  
 `dataOut`  
 [out] Returns an [IEEDataStorage](../vs140/IEEDataStorage.md) object  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method does whatever is necessary to initialize an object so it can return an [IEEDataStorage](../vs140/IEEDataStorage.md) interface on the object's data. This allows the object's data to be viewed and, if allowed, changed by a type visualizer.  
  
## See Also  
 [IPropertyProxyEESide](../vs140/IPropertyProxyEESide.md)   
 [IEEDataStorage](../vs140/IEEDataStorage.md)