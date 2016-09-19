---
title: "IDebugAddress2::GetProcessID"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2c18889d-074a-4b95-87b4-bf1a067f44ed
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugAddress2::GetProcessID
Retrieves the ID of the process that owns the object represented by this [IDebugAddress2](../vs140/IDebugAddress2.md) interface.  
  
## Syntax  
  
```cpp  
HRESULT GetProcessID (  
   DWORD* pProcID  
);  
```  
  
```c#  
int GetProcessID (  
   out uint pProcID  
);  
```  
  
#### Parameters  
 `pProcID`  
 [out] The process ID.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## See Also  
 [IDebugAddress2](../vs140/IDebugAddress2.md)