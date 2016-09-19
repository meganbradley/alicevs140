---
title: "IDebugPortSupplier2::GetPortSupplierName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4c368ab-640d-4b5b-9f74-810dc9364d8f
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortSupplier2::GetPortSupplierName
Gets the port supplier name.  
  
## Syntax  
  
```cpp#  
HRESULT GetPortSupplierName(   
   BSTR* pbstrName  
);  
```  
  
```c#  
int GetPortSupplierName(   
   out string pbstrName  
);  
```  
  
#### Parameters  
 `pbstrName`  
 [out] Returns the name of the port supplier.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugPortSupplier2](../vs140/IDebugPortSupplier2.md)