---
title: "Attaching to the Program"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9a3f5b83-60b5-4ef0-91fe-a432105bd066
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Attaching to the Program
After you have registered your programs with the appropriate port, you must attach the debugger to the program you want to debug.  
  
## Choosing How to Attach  
 There are three ways in which the session debug manager (SDM) attempts to attach to the program being debugged.  
  
1.  For programs that are launched by the debug engine through the [IDebugEngineLaunch2::LaunchSuspended](../vs140/IDebugEngineLaunch2--LaunchSuspended.md) method (typical of interpreted languages, for example), the SDM obtains the [IDebugProgramNodeAttach2](../vs140/IDebugProgramNodeAttach2.md) interface from the [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) object associated with the program being attached to. If the SDM can obtain the `IDebugProgramNodeAttach2` interface, the SDM then calls the [IDebugProgramNodeAttach2::OnAttach](../vs140/IDebugProgramNodeAttach2--OnAttach.md) method. The `IDebugProgramNodeAttach2::OnAttach` method returns `S_OK` to indicate that it did not attach to the program and that other attempts can be made to attach to the program.  
  
2.  If the SDM can obtain the [IDebugProgramEx2](../vs140/IDebugProgramEx2.md) interface from the program being attached to, the SDM calls the [IDebugProgramEx2::Attach](../vs140/IDebugProgramEx2--Attach.md) method. This approach is typical for programs that were launched remotely by the port supplier.  
  
3.  If the program cannot be attached through the `IDebugProgramNodeAttach2::OnAttach` or `IDebugProgramEx2::Attach` methods, the SDM loads the debug engine (if not already loaded) by calling the `CoCreateInstance` function and then calls the [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md) method. This approach is typical for programs launched locally by a port supplier.  
  
     It is also possible for a custom port supplier to call the `IDebugEngine2::Attach` method in the custom port supplier's implementation of the `IDebugProgramEx2::Attach` method. Typically in this case, the custom port supplier launches the debug engine on the remote machine.  
  
 Attachment is achieved when the session debug manager (SDM) calls the [Attach](../vs140/IDebugEngine2--Attach.md) method.  
  
 If you run your DE in the same process as the application to be debugged, then you must implement the following methods of [IDebugProgramNode2](../vs140/IDebugProgramNode2.md):  
  
-   [GetHostName](../vs140/IDebugProgramNode2--GetHostName.md),  
  
-   [GetHostPid](../vs140/IDebugProgramNode2--GetHostPid.md)  
  
-   [GetProgramName](../vs140/IDebugProgramNode2--GetProgramName.md)  
  
 After the `IDebugEngine2::Attach` method is called, follow these steps in your implementation of the `IDebugEngine2::Attach` method:  
  
1.  Send an [IDebugEngineCreateEvent2](../vs140/IDebugEngineCreateEvent2.md) event object to the SDM. For more information, see [Sending Events](../vs140/Sending-Events.md).  
  
2.  Call the [GetProgramId](../vs140/IDebugProgram2--GetProgramId.md) method on the [IDebugProgram2](../vs140/IDebugProgram2.md) object that was passed to the `IDebugEngine2::Attach` method.  
  
     This returns a `GUID` that is used to identify the program. The `GUID` must be stored in the object that represents the local program to the DE, and it must be returned when the `IDebugProgram2::GetProgramId` method is called on the `IDebugProgram2` interface.  
  
    > [!NOTE]
    >  If you implement the `IDebugProgramNodeAttach2` interface, the program's `GUID` is passed to the `IDebugProgramNodeAttach2::OnAttach` method. This `GUID` is used for the program's `GUID` returned by the `IDebugProgram2::GetProgramId` method.  
  
3.  Send an [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md) event object to notify the SDM that the local `IDebugProgram2` object was created to represent the program to the DE. For details, see [Sending Events](../vs140/Sending-Events.md).  
  
    > [!NOTE]
    >  This is not the same `IDebugProgram2` object that was passed into the `IDebugEngine2::Attach` method. The previously passed `IDebugProgram2` object is recognized by the port only and is a separate object.  
  
## See Also  
 [Launch-based Attachment](../vs140/Launch-based-Attachment.md)   
 [Sending Events](../vs140/Sending-Events.md)   
 [IDebugEngineLaunch2::LaunchSuspended](../vs140/IDebugEngineLaunch2--LaunchSuspended.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md)   
 [IDebugProgramNodeAttach2](../vs140/IDebugProgramNodeAttach2.md)   
 [IDebugProgramNodeAttach2::OnAttach](../vs140/IDebugProgramNodeAttach2--OnAttach.md)   
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)   
 [GetProgramId](../vs140/IDebugProgram2--GetProgramId.md)   
 [IDebugProgramEx2](../vs140/IDebugProgramEx2.md)   
 [IDebugProgramEx2::Attach](../vs140/IDebugProgramEx2--Attach.md)   
 [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md)