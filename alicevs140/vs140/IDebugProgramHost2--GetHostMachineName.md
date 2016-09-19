---
title: "IDebugProgramHost2::GetHostMachineName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4677ffe4-aa9b-4450-a63b-74cd3984d956
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramHost2::GetHostMachineName
Gets the name of the machine that the process hosting this program is running on.  
  
## Syntax  
  
```cpp#  
HRESULT GetHostMachineName(   
   BSTR* pbstrHostMachineName  
);  
```  
  
```c#  
int GetHostMachineName(   
   out string pbstrHostMachineName  
);  
```  
  
#### Parameters  
 `pbstrHostMachineName`  
 [out] Returns the name of the machine.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugProgramHost2](../vs140/IDebugProgramHost2.md)