---
title: "IDebugField::GetAddress"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6981bf03-66ef-4bf9-87ea-f6c9624486cb
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugField::GetAddress
This method gets the debug address of a field.  
  
## Syntax  
  
```cpp#  
HRESULT GetAddress(   
   IDebugAddress** ppAddress  
);  
```  
  
```c#  
int GetAddress(  
   out IDebugAddress ppAddress  
);  
```  
  
#### Parameters  
 `ppAddress`  
 [out] Returns the address as an [IDebugAddress](../vs140/IDebugAddress.md) object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, return an error code.  
  
## See Also  
 [IDebugField](../vs140/IDebugField.md)   
 [IDebugAddress](../vs140/IDebugAddress.md)