---
title: "IDebugSymbolProvider::GetNamespacesUsedAtAddress"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 392de54b-9af0-4567-953b-1b41acd1e05c
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSymbolProvider::GetNamespacesUsedAtAddress
This method creates an enumerator for namespaces associated with the debug address.  
  
## Syntax  
  
```cpp#  
HRESULT GetNamespacesUsedAtAddress(   
   IDebugAddress*     pAddress,  
   IEnumDebugFields** ppEnum  
);  
```  
  
```c#  
int GetNamespacesUsedAtAddress(  
   IDebugAddress        pAddress,  
   out IEnumDebugFields ppEnum  
);  
```  
  
#### Parameters  
 `pAddress`  
 [in] The debug address.  
  
 `ppEnum`  
 [out] Returns an [IEnumDebugFields](../vs140/IEnumDebugFields.md) enumerator for the namespaces.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 There may be several namespaces associated with a given debug address, for example, nested namespaces or multiple `using` statements.  
  
## See Also  
 [IDebugSymbolProvider](../vs140/IDebugSymbolProvider.md)   
 [IEnumDebugFields](../vs140/IEnumDebugFields.md)