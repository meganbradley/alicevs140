---
title: "IDebugCoreServer2::GetMachineInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8fa1a1d3-9fcb-4fb3-bf4e-e7172ac08d77
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer2::GetMachineInfo
Retrieves a description of the machine the core server is running on.  
  
## Syntax  
  
```cpp#  
HRESULT GetInfo(   
   MACHINE_INFO_FIELDS Fields,  
   MACHINE_INFO*       pMachineInfo  
);  
```  
  
```c#  
int GetInfo(   
   enum_ MACHINE_INFO_FIELDS  Fields,  
   MACHINE_INFO[]             pMachineInfo  
);  
```  
  
#### Parameters  
 `Fields`  
 [in] A combination of flags from the [MACHINE_INFO_FIELDS](../vs140/MACHINE_INFO_FIELDS.md) enumeration that specify which fields of `pMachineInfo` are to be filled out.  
  
 `pMachineInfo`  
 [in, out] A [MACHINE_INFO](../vs140/MACHINE_INFO.md) structure that is filled in with a description of the machine.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)   
 [MACHINE_INFO_FIELDS](../vs140/MACHINE_INFO_FIELDS.md)   
 [MACHINE_INFO](../vs140/MACHINE_INFO.md)