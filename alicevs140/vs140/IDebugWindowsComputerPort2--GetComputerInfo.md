---
title: "IDebugWindowsComputerPort2::GetComputerInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 654910b2-c239-44c8-92fc-317680a5672f
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugWindowsComputerPort2::GetComputerInfo
Retrieves information about the computer on which the debugger in running.  
  
## Syntax  
  
```cpp#  
HRESULT GetComputerInfo(  
   COMPUTER_INFO * pInfo  
);  
```  
  
```c#  
public int GetComputerInfo(  
   out COMPUTER_INFO[] pInfo  
);  
```  
  
#### Parameters  
 `pInfo`  
 [out] Reference to a structure that contains the computer information.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugWindowsComputerPort2](../vs140/IDebugWindowsComputerPort2.md)   
 [COMPUTER_INFO](../vs140/COMPUTER_INFO.md)