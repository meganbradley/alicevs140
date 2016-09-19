---
title: "IDebugCoreServer2::GetPortSupplier"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: acf181d4-ef42-4aa5-86f9-95fd5467ea31
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer2::GetPortSupplier
Retrieves a specific port supplier.  
  
## Syntax  
  
```cpp#  
HRESULT GetPortSupplier(   
   REFGUID               guidPortSupplier,  
   IDebugPortSupplier2** ppPortSupplier  
);  
```  
  
```c#  
int GetPortSupplier(   
   ref Guid                guidPortSupplier,  
   out IDebugPortSupplier2 ppPortSupplier  
);  
```  
  
#### Parameters  
 `guidPortSupplier`  
 [in] GUID of the port supplier to be retrieved.  
  
 `ppPortSupplier`  
 [out] Returns an [IDebugPortSupplier2](../vs140/IDebugPortSupplier2.md) object representing the desired port supplier.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)   
 [IDebugPortSupplier2](../vs140/IDebugPortSupplier2.md)