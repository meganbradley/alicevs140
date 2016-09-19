---
title: "IDebugCoreServer2::GetMachineName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 693bd794-7215-4f07-8651-b57366d39953
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer2::GetMachineName
Gets the name of the machine the core server is running on.  
  
## Syntax  
  
```cpp#  
HRESULT GetName(   
   BSTR* pbstrName  
);  
```  
  
```c#  
int GetName(   
   out string pbstrName  
);  
```  
  
#### Parameters  
 `pbstrName`  
 [out] Returns a string containing the name of the machine.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)