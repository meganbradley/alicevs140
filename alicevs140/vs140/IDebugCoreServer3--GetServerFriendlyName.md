---
title: "IDebugCoreServer3::GetServerFriendlyName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7035b904-b3d7-4d9b-98d9-65714b8a8b9f
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer3::GetServerFriendlyName
Retrieves a friendly name for the server.  
  
## Syntax  
  
```cpp#  
HRESULT GetServerFriendlyName(  
   BSTR* pbstrName  
);  
```  
  
```c#  
int GetServerFriendlyName(  
   out string pbstrName  
);  
```  
  
#### Parameters  
 `pbstrName`  
 [out] Returns a friendly name for the server.  
  
> [!NOTE]
>  The caller is responsible for freeing the string.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## Remarks  
 For user-launched servers, the name returned by this method is the full name of the server. For auto-launched servers, the name is that of the machine the server is running on.  
  
 For a machine-oriented name, call the [IDebugCoreServer3::GetServerName](../vs140/IDebugCoreServer3--GetServerName.md) method.  
  
## See Also  
 [IDebugCoreServer3](../vs140/IDebugCoreServer3.md)   
 [IDebugCoreServer3::GetServerName](../vs140/IDebugCoreServer3--GetServerName.md)