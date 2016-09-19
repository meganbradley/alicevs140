---
title: "IDebugSymbolProvider::GetContainerField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6b56b4f-a96b-4fa7-87c1-bac4e58fa766
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSymbolProvider::GetContainerField
This method gets the field that contains the debug address.  
  
## Syntax  
  
```cpp#  
HRESULT GetContainerField(   
   IDebugAddress*         pAddress,  
   IDebugContainerField** ppContainerField  
);  
```  
  
```c#  
int GetContainerField(  
   IDebugAddress            pAddress,   
   out IDebugContainerField ppContainerField  
);  
```  
  
#### Parameters  
 `pAddress`  
 [in] The address as represented by an [IDebugAddress](../vs140/IDebugAddress.md) interface.  
  
 `ppContainerField`  
 [out] Returns a container field represented by an [IDebugContainerField](../vs140/IDebugContainerField.md) interface.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugSymbolProvider](../vs140/IDebugSymbolProvider.md)   
 [IDebugAddress](../vs140/IDebugAddress.md)   
 [IDebugContainerField](../vs140/IDebugContainerField.md)