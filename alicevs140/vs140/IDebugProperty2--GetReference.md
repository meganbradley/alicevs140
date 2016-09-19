---
title: "IDebugProperty2::GetReference"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2fa97d9b-c3d7-478e-ba5a-a933f40a0103
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProperty2::GetReference
Returns a reference to the property's value.  
  
## Syntax  
  
```cpp#  
HRESULT GetReference(  
   IDebugReference2** ppReference  
);  
```  
  
```c#  
int GetReference(  
   out IDebugReference2 ppReference  
);  
```  
  
#### Parameters  
 `ppRererence`  
 [out] Returns an [IDebugReference2](../vs140/IDebugReference2.md) object representing a reference to the property's value.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code, typically `E_NOTIMPL` or `E_GETREFERENCE_NO_REFERENCE`.  
  
## See Also  
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IDebugReference2](../vs140/IDebugReference2.md)