---
title: "IDebugProgramNode2::Attach_V7"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b5ffc736-efc7-4ca8-964d-5536ff891b0e
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramNode2::Attach_V7
DEPRECATED. DO NOT USE.  
  
## Syntax  
  
```cpp#  
HRESULT Attach_V7 (   
   IDebugProgram2*       pMDMProgram,  
   IDebugEventCallback2* pCallback,  
   DWORD                 dwReason  
);  
```  
  
```c#  
int Attach_V7 (   
   IDebugProgram2       pMDMProgram,  
   IDebugEventCallback2 pCallback,  
   uint                 dwReason  
);  
```  
  
#### Parameters  
 `pMDMProgram`  
 [in] The [IDebugProgram2](../vs140/IDebugProgram2.md) interface that represents the program to attach to.  
  
 `pCallback`  
 [in] The [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) interface to be used to send debug events to the SDM.  
  
 `dwReason`  
 [in] A value from the [ATTACH_REASON](../vs140/ATTACH_REASON.md) enumeration that specifies the reason for attaching.  
  
## Return Value  
 An implementation should always return `E_NOTIMPL`.  
  
## Remarks  
  
> [!WARNING]
>  As of [!INCLUDE[vsprvslong](../vs140/includes/vsprvslong_md.md)], this method is no longer used and should always return `E_NOTIMPL`. See the [IDebugProgramNodeAttach2](../vs140/IDebugProgramNodeAttach2.md) interface for an alternative approach if the program node needs to indicate it cannot be attached to or if the program node is simply setting the program `GUID`. Otherwise, implement the [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md) method.  
  
## Prior to Visual Studio 2005  
 This method needs to be implemented only if the DE runs in the address space of the program being debugged. Otherwise, this method should return `S_FALSE`.  
  
 When this method is called, the DE must send the [IDebugEngineCreateEvent2](../vs140/IDebugEngineCreateEvent2.md) event object, if it has not already been sent for this instance of the [IDebugEngine2](../vs140/IDebugEngine2.md) interface, as well as the [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md) and [IDebugLoadCompleteEvent2](../vs140/IDebugLoadCompleteEvent2.md) event objects. The [IDebugEntryPointEvent2](../vs140/IDebugEntryPointEvent2.md) event object is then sent if the `dwReason` parameter is `ATTACH_REASON_LAUNCH`.  
  
 The DE must call the [GetProgramId](../vs140/IDebugProgram2--GetProgramId.md) method on the [IDebugProgram2](../vs140/IDebugProgram2.md) object supplied by the [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md) event object, and must store that program's GUID in the instance data for the `IDebugProgram2` object implemented by the DE.  
  
## See Also  
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)   
 [IDebugProgramNodeAttach2](../vs140/IDebugProgramNodeAttach2.md)   
 [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)   
 [IDebugEngineCreateEvent2](../vs140/IDebugEngineCreateEvent2.md)   
 [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md)   
 [IDebugLoadCompleteEvent2](../vs140/IDebugLoadCompleteEvent2.md)   
 [IDebugEntryPointEvent2](../vs140/IDebugEntryPointEvent2.md)   
 [ATTACH_REASON](../vs140/ATTACH_REASON.md)