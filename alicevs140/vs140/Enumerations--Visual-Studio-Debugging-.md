---
title: "Enumerations (Visual Studio Debugging)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 557065bf-081f-4d57-8744-bae02b8a5a6e
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Enumerations (Visual Studio Debugging)
Following are enumerations for the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Debugging SDK.  
  
 [AD_PROCESS_ID_TYPE](../vs140/AD_PROCESS_ID_TYPE.md)  
 Specifies how to interpret a process ID in the [AD_PROCESS_ID](../vs140/AD_PROCESS_ID.md) structure.  
  
 [ADDRESS_KIND](../vs140/ADDRESS_KIND.md)  
 Specifies the types of an address.  
  
 [ASSEMBLYLOCRESOLUTION](../vs140/ASSEMBLYLOCRESOLUTION.md)  
 Specifies where an assembly is located.  
  
 [ATTACH_REASON](../vs140/ATTACH_REASON.md)  
 Specifies the reason for the debug engine (DE) to attach to a program node.  
  
 [BP_COND_STYLE](../vs140/BP_COND_STYLE.md)  
 Specifies the breakpoint condition style for pending and bound breakpoints.  
  
 [BP_ERROR_TYPE](../vs140/BP_ERROR_TYPE.md)  
 Specifies the error type of a breakpoint.  
  
 [BP_FLAGS](../vs140/BP_FLAGS.md)  
 Provides optional flags that may be used to specify additional information when setting a breakpoint.  
  
 [BP_FLAGS90](../vs140/BP_FLAGS90.md)  
 Enumerates valid values for optional flags that may be used to specify additional information when setting a breakpoint. This enumeration extends the [BP_FLAGS](../vs140/BP_FLAGS.md) enumeration.  
  
 [BP_LOCATION_TYPE](../vs140/BP_LOCATION_TYPE.md)  
 Specifies the location type of the breakpoint for a breakpoint request.  
  
 [BP_PASSCOUNT_STYLE](../vs140/BP_PASSCOUNT_STYLE.md)  
 Specifies the condition associated with the breakpoint pass count that will cause the breakpoint to fire.  
  
 [BP_RES_DATA_FLAGS](../vs140/BP_RES_DATA_FLAGS.md)  
 Specifies whether the data breakpoint is being emulated or implemented in hardware.  
  
 [BP_STATE](../vs140/BP_STATE.md)  
 Specifies the existence of a bound breakpoint and whether it is enabled.  
  
 [BP_TYPE](../vs140/BP_TYPE.md)  
 Specifies whether the breakpoint is at a code location, is a data location, or is another type of breakpoint.  
  
 [BP_UNBOUND_REASON](../vs140/BP_UNBOUND_REASON.md)  
 Gives the reason a breakpoint was unbound.  
  
 [BPERESI_FIELDS](../vs140/BPERESI_FIELDS.md)  
 Specifies what information to retrieve about a failed resolution of a breakpoint.  
  
 [BPREQI_FIELDS](../vs140/BPREQI_FIELDS.md)  
 Specifies what information to retrieve about a breakpoint request.  
  
 [BPREQI_FIELDS90](../vs140/BPREQI_FIELDS90.md)  
 Enumerates the valid values that specify the information to be retrieved about a breakpoint request. This enumeration extends the [BPREQI_FIELDS](../vs140/BPREQI_FIELDS.md) enumeration.  
  
 [BPRESI_FIELDS](../vs140/BPRESI_FIELDS.md)  
 Specifies what information is to be retrieved about the successful resolution of a breakpoint.  
  
 [CANSTOP_REASON](../vs140/CANSTOP_REASON.md)  
 Used to determine if a program can stop execution after reaching a particular point in the execution.  
  
 [CONNECTION_PROTOCOL](../vs140/CONNECTION_PROTOCOL.md)  
 A value that indicates the protocol being used to communicate between a debug server and the debug package.  
  
 [CONSTRUCTOR_ENUM](../vs140/CONSTRUCTOR_ENUM.md)  
 Selects different types of constructors.  
  
 [CONTEXT_COMPARE](../vs140/CONTEXT_COMPARE.md)  
 Specifies the criteria for comparing two memory contexts.  
  
 [CONTEXT_INFO_FIELDS](../vs140/CONTEXT_INFO_FIELDS.md)  
 Specifies what information to retrieve about a memory context.  
  
 [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md)  
 Describes various attributes for an [IDebugProperty2](../vs140/IDebugProperty2.md) or an [IDebugReference2](../vs140/IDebugReference2.md) interface.  
  
 [DEBUG_REASON](../vs140/DEBUG_REASON.md)  
 Specifies why the process was launched for debugging.  
  
 [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md)  
 Specifies what information to retrieve about a debug property object.  
  
 [DEBUGREF_INFO_FLAGS](../vs140/DEBUGREF_INFO_FLAGS.md)  
 Specifies what information to retrieve about a debug reference object.  
  
 [DISASSEMBLY_FLAGS](../vs140/DISASSEMBLY_FLAGS.md)  
 Specifies the flags for disassembly.  
  
 [DISASSEMBLY_STREAM_FIELDS](../vs140/DISASSEMBLY_STREAM_FIELDS.md)  
 Specifies what information to retrieve about a disassembly field.  
  
 [DISASSEMBLY_STREAM_SCOPE](../vs140/DISASSEMBLY_STREAM_SCOPE.md)  
 Specifies the scope of the disassembly stream.  
  
 [DisplayKind](../vs140/DisplayKind.md)  
 Enumerates the valid values that represent the kinds of information to take from an an [IDebugField](../vs140/IDebugField.md) object and display to the user.  
  
 [DOCCONTEXT_COMPARE](../vs140/DOCCONTEXT_COMPARE.md)  
 Specifies the criteria for comparing two document contexts.  
  
 [DUMPTYPE](../vs140/DUMPTYPE.md)  
 Specifies how much of a program's state to dump.  
  
 [dwTYPE_KIND](../vs140/dwTYPE_KIND.md)  
 Specifies how to interpret the type of an [IDebugField](../vs140/IDebugField.md) object.  
  
 [EncUnavailableReason](../vs140/EncUnavailableReason.md)  
 Represents the reasons that Edit and Continue is not available.  
  
 [EVALFLAGS](../vs140/EVALFLAGS.md)  
 Specifies flags that control expression evaluation.  
  
 [EVALFLAGS90](../vs140/EVALFLAGS90.md)  
 Enumerates the valid values for flags that control expression evaluation. This enumeration extends the [EVALFLAGS](../vs140/EVALFLAGS.md) enumeration.  
  
 [EVENTATTRIBUTES](../vs140/EVENTATTRIBUTES.md)  
 Specifies the event attributes.  
  
 [EXCEPTION_STATE](../vs140/EXCEPTION_STATE.md)  
 Specifies the exception state.  
  
 [FIELD_INFO_FIELDS](../vs140/FIELD_INFO_FIELDS.md)  
 Specifies what information to retrieve about an [IDebugField](../vs140/IDebugField.md) object.  
  
 [FIELD_KIND](../vs140/FIELD_KIND.md)  
 Specifies the kind of field contained in an [IDebugField](../vs140/IDebugField.md) object.  
  
 [FIELD_KIND_EX](../vs140/FIELD_KIND_EX.md)  
 Enumerates additional kinds of fields an [IDebugField](../vs140/IDebugField.md) object can contain. This enumeration extends the [FIELD_KIND](../vs140/FIELD_KIND.md) enumeration.  
  
 [FIELD_MODIFIERS](../vs140/FIELD_MODIFIERS.md)  
 Specifies modifiers for a field type.  
  
 [FRAMEINFO_FLAGS](../vs140/FRAMEINFO_FLAGS.md)  
 Specifies the information to retrieve about a stack frame object.  
  
 [GETHOSTNAME_TYPE](../vs140/GETHOSTNAME_TYPE.md)  
 Specifies the type of host name.  
  
 [GETNAME_TYPE](../vs140/GETNAME_TYPE.md)  
 Specifies the name type of files to retrieve.  
  
 [INTERCEPT_EXCEPTION_ACTION](../vs140/INTERCEPT_EXCEPTION_ACTION.md)  
 Specifies what actions to take when intercepting exceptions.  
  
 [LAUNCH_FLAGS](../vs140/LAUNCH_FLAGS.md)  
 Specifies how a program is to be launched.  
  
 [MACHINE_INFO_FIELDS](../vs140/MACHINE_INFO_FIELDS.md)  
 Specifies what kind of information to retrieve for a particular machine.  
  
 [MACHINE_INFO_FLAGS](../vs140/MACHINE_INFO_FLAGS.md)  
 Used to describe a machine.  
  
 [MESSAGETYPE](../vs140/MESSAGETYPE.md)  
 Specifies the message type and reason.  
  
 [MODULE_FLAGS](../vs140/MODULE_FLAGS.md)  
 Used to describe a module.  
  
 [MODULE_INFO_FIELDS](../vs140/MODULE_INFO_FIELDS.md)  
 Specifies the flags for the debug module information.  
  
 [MODULE_INFO_FLAGS](../vs140/MODULE_INFO_FLAGS.md)  
 Specifies the state of symbols for a module.  
  
 [NAME_MATCH](../vs140/NAME_MATCH.md)  
 Selects the case option for matching names.  
  
 [OBJECT_TYPE](../vs140/OBJECT_TYPE.md)  
 Specifies the type of an object from the expression evaluator.  
  
 [PARSEFLAGS](../vs140/PARSEFLAGS.md)  
 Specifies how to parse an expression.  
  
 [PENDING_BP_STATE](../vs140/PENDING_BP_STATE.md)  
 Specifies the state of a pending breakpoint (a breakpoint that has not yet been bound).  
  
 [PENDING_BP_STATE_FLAGS](../vs140/PENDING_BP_STATE_FLAGS.md)  
 Specifies the pending breakpoint state flags.  
  
 [PORT_SUPPLIER_DESCRIPTION_FLAGS](../vs140/PORT_SUPPLIER_DESCRIPTION_FLAGS.md)  
 Defines the metadata that can be retrieved about a port supplier.  
  
 [PROCESS_INFO_FIELDS](../vs140/PROCESS_INFO_FIELDS.md)  
 Specified what kind of information to retrieve for a process.  
  
 [PROCESS_INFO_FLAGS](../vs140/PROCESS_INFO_FLAGS.md)  
 Describes or specifies properties of a process.  
  
 [PROGRAM_DESTROY_FLAGS](../vs140/PROGRAM_DESTROY_FLAGS.md)  
 Enumerates the valid values of the program destroy flags.  
  
 [PROVIDER_FIELDS](../vs140/PROVIDER_FIELDS.md)  
 Specifies properties associated with a program provider.  
  
 [PROVIDER_FLAGS](../vs140/PROVIDER_FLAGS.md)  
 Specifies desired properties to be obtained from a program provider.  
  
 [REFERENCE_COMPARE](../vs140/REFERENCE_COMPARE.md)  
 Specifies the type of comparison for references.  
  
 [REFERENCE_TYPE](../vs140/REFERENCE_TYPE.md)  
 Specifies the reference type.  
  
 [SEEK_START](../vs140/SEEK_START.md)  
 Specifies the position from which to start seeking in a disassembly.  
  
 [STEPKIND](../vs140/STEPKIND.md)  
 Specifies the step kind for stepping.  
  
 [STEPUNIT](../vs140/STEPUNIT.md)  
 Specifies the step unit for stepping.  
  
 [SYMBOL_SEARCH_INFO_FIELDS](../vs140/SYMBOL_SEARCH_INFO_FIELDS.md)  
 Specifies what kind of symbol information to retrieve.  
  
 [TEXT_DOC_ATTR_2](../vs140/TEXT_DOC_ATTR_2.md)  
 Describes the attributes of a document.  
  
 [THREADPROPERTY_FIELDS](../vs140/THREADPROPERTY_FIELDS.md)  
 Specifies what information about a thread that is to be retrieved.  
  
 [THREADSTATE](../vs140/THREADSTATE.md)  
 Specifies the state of the thread.  
  
## Requirements  
 Header: msdbg.h, sh.h, or ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [API Reference](../vs140/API-Reference--Visual-Studio-Debugging-.md)