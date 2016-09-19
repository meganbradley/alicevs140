---
title: "IDebugProgramNode2::GetHostMachineName_V7"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a992f2c9-f68b-4146-8cc2-027753bf7ce6
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramNode2::GetHostMachineName_V7
DEPRECATED. DO NOT USE.  
  
## Syntax  
  
```cpp#  
HRESULT GetHostMachineName_V7 (   
   BSTR* pbstrHostMachineName  
);  
```  
  
```c#  
int GetHostMachineName_V7 (   
   out string pbstrHostMachineName  
);  
```  
  
#### Parameters  
 `pbstrHostMachineName`  
 [out] Returns the name of the machine in which the program is running.  
  
## Return Value  
 An implementation should always return `E_NOTIMPL`.  
  
## Remarks  
  
> [!WARNING]
>  As of [!INCLUDE[vsprvslong](../vs140/includes/vsprvslong_md.md)], this method is no longer used and should always return `E_NOTIMPL`.  
  
## See Also  
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)