---
title: "IDebugCoreServer2::EnumPortSuppliers"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ce0c90e4-8e02-4b08-b558-7677fb2c88f7
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer2::EnumPortSuppliers
Retrieves a list of all available port suppliers.  
  
## Syntax  
  
```cpp#  
HRESULT EnumPortSuppliers(  
   IEnumDebugPortSuppliers2** ppEnum  
);  
```  
  
```c#  
int EnumPortSuppliers(  
   out IEnumDebugPortSuppliers2 ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns an [IEnumDebugPortSuppliers2](../vs140/IEnumDebugPortSuppliers2.md) object that contains a list of all port suppliers.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)   
 [IEnumDebugPortSuppliers2](../vs140/IEnumDebugPortSuppliers2.md)