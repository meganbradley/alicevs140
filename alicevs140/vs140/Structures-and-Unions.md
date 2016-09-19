---
title: "Structures and Unions"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9ff0a8f8-1ee6-4fdd-8b80-206436ff589b
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Structures and Unions
The following are structures and unions in the Visual Studio Debugging SDK.  
  
 [AD_PROCESS_ID](../vs140/AD_PROCESS_ID.md)  
 Specifies the process ID, which may be either a system ID or a GUID.  
  
 [BP_CONDITION](../vs140/BP_CONDITION.md)  
 Describes the conditions under which a breakpoint will fire.  
  
 [BP_ERROR_RESOLUTION_INFO](../vs140/BP_ERROR_RESOLUTION_INFO.md)  
 Describes the resolution of an error breakpoint, including location, program, and thread.  
  
 [BP_LOCATION](../vs140/BP_LOCATION.md)  
 Specifies the type of structure used to describe the location of the breakpoint.  
  
 [BP_LOCATION_CODE_ADDRESS](../vs140/BP_LOCATION_CODE_ADDRESS.md)  
 Defines the components that describe the location of a breakpoint at an address in code.  
  
 [BP_LOCATION_CODE_CONTEXT](../vs140/BP_LOCATION_CODE_CONTEXT.md)  
 Describes the location of a breakpoint that is bound directly to an address in the program being debugged.  
  
 [BP_LOCATION_CODE_FILE_LINE](../vs140/BP_LOCATION_CODE_FILE_LINE.md)  
 Describes the location of a breakpoint at line in a code source file.  
  
 [BP_LOCATION_CODE_FUNC_OFFSET](../vs140/BP_LOCATION_CODE_FUNC_OFFSET.md)  
 Describes the offset location of a breakpoint at a function in code.  
  
 [BP_LOCATION_CODE_STRING](../vs140/BP_LOCATION_CODE_STRING.md)  
 Used for setting code breakpoints based on a string that the user can enter from the IDE.  
  
 [BP_LOCATION_DATA_STRING](../vs140/BP_LOCATION_DATA_STRING.md)  
 Used for setting data breakpoints that are based on a string that the user can enter from the IDE.  
  
 [BP_LOCATION_RESOLUTION](../vs140/BP_LOCATION_RESOLUTION.md)  
 Describes the resolution of a breakpoint at a specific location.  
  
 [BP_PASSCOUNT](../vs140/BP_PASSCOUNT.md)  
 Describes the count and conditions upon which a breakpoint will be fired after having been previously passed.  
  
 [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md)  
 Contains the information required to implement a breakpoint.  
  
 [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md)  
 Contains the information required to implement a breakpoint (same as the [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md) structure but includes vendor GUID, constraint and tracepoint information).  
  
 [BP_RESOLUTION_CODE](../vs140/BP_RESOLUTION_CODE.md)  
 Describes the location of a code breakpoint.  
  
 [BP_RESOLUTION_DATA](../vs140/BP_RESOLUTION_DATA.md)  
 Describes the result of binding a data breakpoint.  
  
 [BP_RESOLUTION_INFO](../vs140/BP_RESOLUTION_INFO.md)  
 Describes the bound breakpoint information for either a code breakpoint or a data breakpoint.  
  
 [BP_RESOLUTION_LOCATION](../vs140/BP_RESOLUTION_LOCATION.md)  
 Specifies the structure of the breakpoint resolution location.  
  
 [BSTR_ARRAY](../vs140/BSTR_ARRAY.md)  
 Describes an array of strings.  
  
 [BUILT_TYPE](../vs140/BUILT_TYPE.md)  
 Specifies information about a field type taken from metadata.  
  
 [CODE_PATH](../vs140/CODE_PATH.md)  
 Describes a call to a function or method.  
  
 [COMPUTER_INFO](../vs140/COMPUTER_INFO.md)  
 Describes the computer on which the debugger is running.  
  
 [CONST_GUID_ARRAY](../vs140/CONST_GUID_ARRAY.md)  
 Describes a list of GUIDs.  
  
 [CONTEXT_INFO](../vs140/CONTEXT_INFO.md)  
 Describes a memory context or code context.  
  
 [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md)  
 Describes an address in a program being debugged.  
  
 [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md)  
 Represents one of a number of different kinds of addresses.  
  
 [DEBUG_CUSTOM_VIEWER](../vs140/DEBUG_CUSTOM_VIEWER.md)  
 Identifies a custom viewer or type visualizer.  
  
 [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md)  
 Describes a debug property that in turn describes an object of a hierarchical nature that has name, type, and value.  
  
 [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md)  
 Describes a reference.  
  
 [DisassemblyData](../vs140/DisassemblyData.md)  
 Describes disassembly to the IDE for display.  
  
 [EXCEPTION_INFO](../vs140/EXCEPTION_INFO.md)  
 Describes an exception or run-time error thrown by the program being debugged.  
  
 [FIELD_INFO](../vs140/FIELD_INFO.md)  
 Describes a local variable, parameter, or other field.  
  
 [FRAMEINFO](../vs140/FRAMEINFO.md)  
 Describes a stack frame.  
  
 [GUID_ARRAY](../vs140/GUID_ARRAY.md)  
 Describes an array of unique identifiers for available debug engines.  
  
 [JMC_CODE_SPEC](../vs140/JMC_CODE_SPEC.md)  
 Used to set the JustMyCode information for a module.  
  
 [MACHINE_INFO](../vs140/MACHINE_INFO.md)  
 Describes a particular machine.  
  
 [METADATA_ADDRESS_ARRAYELEM](../vs140/METADATA_ADDRESS_ARRAYELEM.md)  
 Describes an array element within an array.  
  
 [METADATA_ADDRESS_FIELD](../vs140/METADATA_ADDRESS_FIELD.md)  
 Describes the address of a field of a class or structure.  
  
 [METADATA_ADDRESS_LOCAL](../vs140/METADATA_ADDRESS_LOCAL.md)  
 Describes the address of a local variable within a scope (usually a function or method).  
  
 [METADATA_ADDRESS_METHOD](../vs140/METADATA_ADDRESS_METHOD.md)  
 Describes the address of a method of a class.  
  
 [METADATA_ADDRESS_PARAM](../vs140/METADATA_ADDRESS_PARAM.md)  
 Describes a parameter of a method or function.  
  
 [METADATA_ADDRESS_RETVAL](../vs140/METADATA_ADDRESS_RETVAL.md)  
 Describes a return value from a method or function.  
  
 [METADATA_TYPE](../vs140/METADATA_TYPE.md)  
 Describes a field type taken from metadata.  
  
 [MODULE_INFO](../vs140/MODULE_INFO.md)  
 Describes a particular module (DLL, EXE, or assembly).  
  
 [MODULE_SYMBOL_SEARCH_INFO](../vs140/MODULE_SYMBOL_SEARCH_INFO.md)  
 Describes status information about symbol search paths that have been searched.  
  
 [NATIVE_ADDRESS](../vs140/NATIVE_ADDRESS.md)  
 Describes a native address.  
  
 [PDB_TYPE](../vs140/PDB_TYPE.md)  
 Describes a field type taken from a PDB symbol.  
  
 [PENDING_BP_STATE_INFO](../vs140/PENDING_BP_STATE_INFO.md)  
 Describes the state of a breakpoint that is ready to bind to a code location.  
  
 [PROCESS_INFO](../vs140/PROCESS_INFO.md)  
 Describes a process.  
  
 [PROGRAM_NODE_ARRAY](../vs140/PROGRAM_NODE_ARRAY.md)  
 Describes a list of [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) objects that represent program nodes.  
  
 [PROVIDER_PROCESS_DATA](../vs140/PROVIDER_PROCESS_DATA.md)  
 Describes processes running on a machine.  
  
 [TEXT_POSITION](../vs140/TEXT_POSITION.md)  
 Describes the line and column location in the given text.  
  
 [THREADPROPERTIES](../vs140/THREADPROPERTIES.md)  
 Describes the properties of a thread.  
  
 [TYPE_INFO](../vs140/TYPE_INFO.md)  
 Describes a field's type.  
  
 [UNMANAGED_ADDRESS_PHYSICAL](../vs140/UNMANAGED_ADDRESS_PHYSICAL.md)  
 Describes a physical address.  
  
 [UNMANAGED_ADDRESS_THIS_RELATIVE](../vs140/UNMANAGED_ADDRESS_THIS_RELATIVE.md)  
 Describes an address that is relative to a `this` pointer (`Me` in Visual Basic).  
  
## Requirements  
 Header: msdbg.h, sh.h, or ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [API Reference](../vs140/API-Reference--Visual-Studio-Debugging-.md)