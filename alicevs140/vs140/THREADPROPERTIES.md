---
title: "THREADPROPERTIES"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7d397207-db03-4ec0-9f79-3794056ed89f
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# THREADPROPERTIES
Describes the properties of a thread.  
  
## Syntax  
  
```cpp#  
typedef struct _tagTHREADPROPERTIES {   
   THREADPROPERTY_FIELDS dwFields;  
   DWORD                 dwThreadId;  
   DWORD                 dwSuspendCount;  
   DWORD                 dwThreadState;  
   BSTR                  bstrPriority;  
   BSTR                  bstrName;  
   BSTR                  bstrLocation;  
} THREADPROPERTIES;  
```  
  
```c#  
public struct THREADPROPERTIES {   
   public uint   dwFields;  
   public uint   dwThreadId;  
   public uint   dwSuspendCount;  
   public uint   dwThreadState;  
   public string bstrPriority;  
   public string bstrName;  
   public string bstrLocation;  
};  
```  
  
## Members  
 dwFields  
 A combination of flags from the [THREADPROPERTY_FIELDS](../vs140/THREADPROPERTY_FIELDS.md) enumeration, describing which fields in this structure are valid.  
  
 dwThreadId  
 The thread ID.  
  
 dwSuspendCount  
 The thread suspend count.  
  
 dwThreadState  
 A value from the [THREADSTATE](../vs140/THREADSTATE.md) enumeration indicating the state of the operating thread.  
  
 bstrPriority  
 A string specifying the thread priority; for example, "Above Normal", "Normal", or "Time Critical".  
  
 bstName  
 The thread name.  
  
 bstrLocation  
 The thread location (usually the topmost stack frame), typically expressed as the name of the method where execution is currently halted.  
  
## Remarks  
 This structure is filled in by a call to the [GetThreadProperties](../vs140/IDebugThread2--GetThreadProperties.md) method. The information so returned is typically used in populating the **Threads** window.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [GetThreadProperties](../vs140/IDebugThread2--GetThreadProperties.md)   
 [THREADPROPERTY_FIELDS](../vs140/THREADPROPERTY_FIELDS.md)   
 [THREADSTATE](../vs140/THREADSTATE.md)