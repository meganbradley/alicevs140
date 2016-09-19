---
title: "BP_RES_DATA_FLAGS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d97611e2-def6-45a9-ad7d-eedf2ad4c82b
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_RES_DATA_FLAGS
Specifies whether the data breakpoint is being emulated or implemented in hardware.  
  
## Syntax  
  
```cpp#  
enum enum_BP_RES_DATA_FLAGS {   
   BP_RES_DATA_EMULATED = 0x0001  
};  
typedef DWORD BP_RES_DATA_FLAGS;  
```  
  
```c#  
public enum enum_BP_RES_DATA_FLAGS {   
   BP_RES_DATA_EMULATED = 0x0001  
};  
```  
  
## Members  
 BP_RES_DATA_EMULATED  
 Specifies that the data breakpoint is being emulated.  
  
## Remarks  
 Used for the `dwFlags` member of the [BP_RESOLUTION_DATA](../vs140/BP_RESOLUTION_DATA.md) structure.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [BP_RESOLUTION_DATA](../vs140/BP_RESOLUTION_DATA.md)