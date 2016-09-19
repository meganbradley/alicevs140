---
title: "IDebugProcess3::DisableENC"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cffdbdac-4d76-4aeb-aa55-5d0410db99f1
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess3::DisableENC
This method explicitly disables Edit and Continue on this process (and all programs it contains). A custom port supplier should always return `E_NOTIMPL`.  
  
## Syntax  
  
```cpp  
HRESULT DisableENC(  
   EncUnavailableReason reason  
);  
```  
  
```c#  
   EncUnavailableReason reason  
);  
```  
  
#### Parameters  
 `reason`  
 [in] A value from the [EncUnavailableReason](../vs140/EncUnavailableReason.md) enumeration.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
> [!NOTE]
>  A custom port supplier should always return `E_NOTIMPL`.  
  
## Remarks  
 Once Edit and Continue is disabled for a process, it can be re-enabled only by restarting the process.  
  
## See Also  
 [IDebugProcess3](../vs140/IDebugProcess3.md)   
 [EncUnavailableReason](../vs140/EncUnavailableReason.md)