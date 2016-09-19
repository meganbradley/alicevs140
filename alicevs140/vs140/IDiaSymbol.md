---
title: "IDiaSymbol"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 01ad328a-736c-4933-a9f8-c2ded19ddd8c
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol
Describes the properties of a symbol instance.  
  
## Syntax  
  
```  
IDiaSymbol : IUnknown  
```  
  
## Methods in Alphabetical Order  
 The following table shows the methods of `IDiaSymbol`.  
  
> [!NOTE]
>  Symbols will return meaningful data for only some of these methods, depending on the type of symbol. If a method returns `S_OK`, then that method has returned meaningful data.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaSymbol::findChildren](../vs140/IDiaSymbol--findChildren.md)|Retrieves all children of the symbol.|  
|[findChildrenEx](../vs140/IDiaSymbol--findChildrenEx.md)|Retrieves the children of the symbol. This method is the extended version of [IDiaSymbol::findChildren](../vs140/IDiaSymbol--findChildren.md).|  
|[findChildrenExByAddr](../vs140/IDiaSymbol--findChildrenExByAddr.md)|Retrieves the children of the symbol that are valid at a specified address.|  
|[findChildrenExByRVA](../vs140/IDiaSymbol--findChildrenExByRVA.md)|Retrieves the children of the symbol that are valid at a specified relative virtual address (RVA).|  
|[findChildrenExByVA](../vs140/IDiaSymbol--findChildrenExByVA.md)|Retrieves the children of the symbol that are valid at a specified virtual address.|  
|[findInlineFramesByAddr](../vs140/IDiaSymbol--findInlineFramesByAddr.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a given address.|  
|[findInlineFramesByRVA](../vs140/IDiaSymbol--findInlineFramesByRVA.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a specified relative virtual address (RVA).|  
|[findInlineFramesByVA](../vs140/IDiaSymbol--findInlineFramesByVA.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a specified virtual address (VA).|  
|[findInlineeLines](../vs140/IDiaSymbol--findInlineeLines.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol.|  
|[findInlineeLinesByAddr](../vs140/IDiaSymbol--findInlineeLinesByAddr.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol within the specified address range.|  
|[findInlineeLinesByRVA](../vs140/IDiaSymbol--findInlineeLinesByRVA.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol within the specified relative virtual address (RVA).|  
|[findInlineeLinesByVA](../vs140/IDiaSymbol--findInlineeLinesByVA.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol within the specified virtual address (VA).|  
|[findSymbolsByRVAForAcceleratorPointerTag](../vs140/IDiaSymbol--findSymbolsByRVAForAcceleratorPointerTag.md)|Given a corresponding tag value, this method returns an enumeration of symbols that are contained in this stub function at a specified relative virtual address.|  
|[findSymbolsForAcceleratorPointerTags](../vs140/IDiaSymbol--findSymbolsForAcceleratorPointerTag.md)|Returns the number of accelerator pointer tags in a C++ AMP stub function.|  
|[get_acceleratorPointerTags](../vs140/IDiaSymbol--get_acceleratorPointerTags.md)|Returns all accelerator pointer tag values that correspond to a C++ AMP accelerator stub function.|  
|[IDiaSymbol::get_access](../vs140/IDiaSymbol--get_access.md)|Retrieves the access modifier of a class member.|  
|[IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md)|Retrieves the offset part of an address location.|  
|[IDiaSymbol::get_addressSection](../vs140/IDiaSymbol--get_addressSection.md)|Retrieves the section part of an address location.|  
|[IDiaSymbol::get_addressTaken](../vs140/IDiaSymbol--get_addressTaken.md)|Retrieves a flag indicating whether another symbol references this address.|  
|[IDiaSymbol::get_age](../vs140/IDiaSymbol--get_age.md)|Retrieves the age value of a program database.|  
|[IDiaSymbol::get_arrayIndexType](../vs140/IDiaSymbol--get_arrayIndexType.md)|Retrieves the symbol identifier of the array index type.|  
|[IDiaSymbol::get_arrayIndexTypeId](../vs140/IDiaSymbol--get_arrayIndexTypeId.md)|Retrieves the array index type identifier of the symbol.|  
|[IDiaSymbol::get_backEndMajor](../vs140/IDiaSymbol--get_backEndMajor.md)|Retrieves the back-end major version number.|  
|[IDiaSymbol::get_backEndMinor](../vs140/IDiaSymbol--get_backEndMinor.md)|Retrieves the back-end minor version number.|  
|[IDiaSymbol::get_backEndBuild](../vs140/IDiaSymbol--get_backEndBuild.md)|Retrieves the back-end build number.|  
|[get_baseDataOffset](../vs140/IDiaSymbol--get_baseDataOffset.md)|Retrieves the base data offset.|  
|[get_baseDataSlot](../vs140/IDiaSymbol--get_baseDataSlot.md)|Retrieves the base data slot.|  
|[get_baseSymbol](../vs140/IDiaSymbol--get_baseSymbol.md)|Retrieves the symbol from which the pointer is based.|  
|[get_baseSymbolId](../vs140/IDiaSymbol--get_baseSymbolId.md)|Retrieves the symbol ID from which the pointer is based.|  
|[IDiaSymbol::get_baseType](../vs140/IDiaSymbol--get_baseType.md)|Retrieves the type tag of a simple type.|  
|[IDiaSymbol::get_bitPosition](../vs140/IDiaSymbol--get_bitPosition.md)|Retrieves the bit position of a location.|  
|[get_builtInKind](../vs140/IDiaSymbol--get_builtInKind.md)|Retrieves a built-in kind of the HLSL type.|  
|[IDiaSymbol::get_callingConvention](../vs140/IDiaSymbol--get_callingConvention.md)|Returns an indicator of a method's calling convention.|  
|[IDiaSymbol::get_classParent](../vs140/IDiaSymbol--get_classParent.md)|Retrieves a reference to the class parent of the symbol.|  
|[IDiaSymbol::get_classParentId](../vs140/IDiaSymbol--get_classParentId.md)|Retrieves the class parent identifier of the symbol.|  
|[IDiaSymbol::get_code](../vs140/IDiaSymbol--get_code.md)|Retrieves a flag indicating whether the symbol refers to a code address.|  
|[IDiaSymbol::get_compilerGenerated](../vs140/IDiaSymbol--get_compilerGenerated.md)|Retrieves a flag indicating whether the symbol was compiler-generated.|  
|[get_compilerName](../vs140/IDiaSymbol--get_compilerName.md)|Retrieves the name of the compiler used to create the [Compiland](../vs140/Compiland.md).|  
|[IDiaSymbol::get_constructor](../vs140/IDiaSymbol--get_constructor.md)|Retrieves a flag indicating whether the user-defined data type has a constructor.|  
|[IDiaSymbol::get_container](../vs140/IDiaSymbol--get_container.md)|Retrieves the containing symbol of this symbol.|  
|[IDiaSymbol::get_constType](../vs140/IDiaSymbol--get_constType.md)|Retrieves a flag indicating whether the user-defined data type is constant.|  
|[IDiaSymbol::get_count](../vs140/IDiaSymbol--get_count.md)|Retrieves the number of items in a list or array.|  
|[get_countLiveRanges](../vs140/IDiaSymbol--get_countLiveRanges.md)|Retrieves the number of valid address ranges associated with the local symbol.|  
|[get_customCallingConvention](../vs140/IDiaSymbol--get_customCallingConvention.md)|Retrieves a flag indicating whether the function uses a custom calling convention.|  
|[IDiaSymbol::get_dataBytes](../vs140/IDiaSymbol--get_dataBytes.md)|Retrieves the data bytes of an OEM symbol.|  
|[IDiaSymbol::get_dataKind](../vs140/IDiaSymbol--get_dataKind.md)|Retrieves the variable classification of a data symbol.|  
|[IDiaSymbol::get_editAndContinueEnabled](../vs140/IDiaSymbol--get_editAndContinueEnabled.md)|Retrieves the flag describing the Edit and Continue features of the compiled program or unit.|  
|[get_farReturn](../vs140/IDiaSymbol--get_farReturn.md)|Retrieves a flag indicating whether the function uses a far return.|  
|[IDiaSymbol::get_frontEndMajor](../vs140/IDiaSymbol--get_frontEndMajor.md)|Retrieves the front-end major version number.|  
|[IDiaSymbol::get_frontEndMinor](../vs140/IDiaSymbol--get_frontEndMinor.md)|Retrieves the front-end minor version number.|  
|[IDiaSymbol::get_frontEndBuild](../vs140/IDiaSymbol--get_frontEndBuild.md)|Retrieves the front-end build number.|  
|[IDiaSymbol::get_function](../vs140/IDiaSymbol--get_function.md)|Retrieves a flag indicating whether the public symbol refers to a function.|  
|[IDiaSymbol::get_guid](../vs140/IDiaSymbol--get_guid.md)|Retrieves the symbol's GUID.|  
|[get_hasAlloca](../vs140/IDiaSymbol--get_hasAlloca.md)|Retrieves a flag indicating whether the function contains a call to `alloca`.|  
|[IDiaSymbol::get_hasAssignmentOperator](../vs140/IDiaSymbol--get_hasAssignmentOperator.md)|Retrieves a flag indicating whether the user-defined data type has any assignment operators defined.|  
|[IDiaSymbol::get_hasCastOperator](../vs140/IDiaSymbol--get_hasCastOperator.md)|Retrieves a flag indicating whether the user-defined data type has any cast operators defined.|  
|[get_hasDebugInfo](../vs140/IDiaSymbol--get_hasDebugInfo.md)|Retrieves a flag indicating whether the compiland contains any debugging information.|  
|[get_hasEH](../vs140/IDiaSymbol--get_hasEH.md)|Retrieves a flag indicating whether the function has a C++-style exception handler.|  
|[get_hasEHa](../vs140/IDiaSymbol--get_hasEHa.md)|Retrieves a flag indicating whether the function has an asynchronous exception handler.|  
|[get_hasInlAsm](../vs140/IDiaSymbol--get_hasInlAsm.md)|Retrieves a flag indicating whether the function has inline assembly.|  
|[get_hasLongJump](../vs140/IDiaSymbol--get_hasLongJump.md)|Retrieves a flag indicating whether the function contains a longjmp command (part of C-style exception handling).|  
|[get_hasManagedCode](../vs140/IDiaSymbol--get_hasManagedCode.md)|Retrieves a flag indicating whether the module contains managed code.|  
|[IDiaSymbol::get_hasNestedTypes](../vs140/IDiaSymbol--get_hasNestedTypes.md)|Retrieves a flag indicating whether the user-defined data type has nested type definitions.|  
|[get_hasSecurityChecks](../vs140/IDiaSymbol--get_hasSecurityChecks.md)|Retrieves a flag indicating whether the function or compiland has security checks compiled in (via the [/GS (Buffer Security Check)](../Topic/-GS%20\(Buffer%20Security%20Check\).md) compiler switch).|  
|[get_hasSEH](../vs140/IDiaSymbol--get_hasSEH.md)|Retrieves a flag indicating whether the function has Win32-style Structured Exception Handling.|  
|[get_hasSetJump](../vs140/IDiaSymbol--get_hasSetJump.md)|Retrieves a flag indicating whether the function contains a setjmp command.|  
|[IDiaSymbol::get_indirectVirtualBaseClass](../vs140/IDiaSymbol--get_indirectVirtualBaseClass.md)|Retrieves a flag indicating whether the user-defined data type is an indirect virtual base class.|  
|[get_InlSpec](../vs140/IDiaSymbol--get_InlSpec.md)|Retrieves a flag indicating whether the function has been marked with the inline attribute.|  
|[get_interruptReturn](../vs140/IDiaSymbol--get_interruptReturn.md)|Retrieves a flag indicating whether the function has a return from interrupt instruction.|  
|[IDiaSymbol::get_intro](../vs140/IDiaSymbol--get_intro.md)|Retrieves a flag indicating whether the function is the base class virtual function.|  
|[get_isAcceleratorGroupSharedLocal](../vs140/IDiaSymbol--get_isAcceleratorGroupSharedLocal.md)|Retrieves a flag that indicates whether the symbol corresponds to a group shared local variable in code compiled for a C++ AMP Accelerator.|  
|[get_isAcceleratorPointerTagLiveRange](../vs140/IDiaSymbol--get_isAcceleratorPointerTagLiveRange.md)|Retrieves a flag that indicates whether the symbol corresponds to the *definition range symbol* for the tag component of a pointer variable in code compiled for a C++ AMP Accelerator. The definition range symbol is the location of a variable for a span of addresses.|  
|[get_isAcceleratorStubFunction](../vs140/IDiaSymbol--get_isAcceleratorStubFunction.md)|Indicates whether the symbol corresponds to a top-level function symbol for a shader compiled for an accelerator that corresponds to a `parallel_for_each` call.|  
|[get_isAggregated](../vs140/IDiaSymbol--get_isAggregated.md)|Retrieves a flag indicating whether the data is part of an aggregate of many symbols.|  
|[get_isCTypes](../vs140/IDiaSymbol--get_isCTypes.md)|Retrieves a flag indicating whether the symbol file contains C types.|  
|[get_isCVTCIL](../vs140/IDiaSymbol--get_isCVTCIL.md)|Retrieves a flag indicating whether the module was converted from Common Intermediate Language (CIL) to native code.|  
|[get_isDataAligned](../vs140/IDiaSymbol--get_isDataAligned.md)|Retrieves a flag indicating whether the elements of a user-defined data type are aligned to a specific boundary.|  
|[get_isHLSLData](../vs140/IDiaSymbol--get_isHLSLData.md)|Specifies whether this symbol represents High Level Shader Language (HLSL) data.|  
|[get_isHotpatchable](../vs140/IDiaSymbol--get_isHotpatchable.md)|Retrieves a flag indicating whether the module was compiled with the [/hotpatch (Create Hotpatchable Image)](../Topic/-hotpatch%20\(Create%20Hotpatchable%20Image\).md) compiler switch.|  
|[get_isLTCG](../vs140/IDiaSymbol--get_isLTCG.md)|Retrieves a flag indicating whether the managed compiland was linked with the linker's LTCG.|  
|[get_isMatrixRowMajor](../vs140/IDiaSymbol--get_isMatrixRowMajor.md)|Specifies whether the matrix is row major.|  
|[get_isMSILNetmodule](../vs140/IDiaSymbol--get_isMSILNetmodule.md)|Retrieves a flag indicating whether the managed compiland is a .netmodule (containing only metadata).|  
|[get_isMultipleInheritance](../vs140/IDiaSymbol--get_isMultipleInheritance.md)|Specifies whether the `this` pointer points to a data member with multiple inheritance.|  
|[get_isNaked](../vs140/IDiaSymbol--get_isNaked.md)|Retrieves a flag indicating whether the function has the [naked (C++)](../vs140/naked--C---.md) attribute.|  
|[get_isOptimizedAway](../vs140/IDiaSymbol--get_isOptimizedAway.md)|Specifies whether the variable is optimized away.|  
|[get_isPointerBasedOnSymbolValue](../vs140/IDiaSymbol--get_isPointerBasedOnSymbolValue.md)|Specifies whether the `this` pointer is based on a symbol value.|  
|[get_isPointerToDataMember](../vs140/IDiaSymbol--get_isPointerToDataMember.md)|Specifies whether this symbol is a pointer to a data member.|  
|[get_isPointerToMemberFunction](../vs140/IDiaSymbol--get_isPointerToMemberFunction.md)|Specifies whether this symbol is a pointer to a member function.|  
|[get_isReturnValue](../vs140/IDiaSymbol--get_isReturnValue.md)|Specifies whether the variable carries a return value.|  
|[get_isSdl](../vs140/IDiaSymbol--get_isSdl.md)|Specifies whether the module is compiled with the /SDL option.|  
|[get_isSingleInheritance](../vs140/IDiaSymbol--get_isSingleInheritance.md)|Specifies whether the `this` pointer points to a data member with single inheritance.|  
|[get_isSplitted](../vs140/IDiaSymbol--get_isSplitted.md)|Retrieves a flag indicating whether the data has been split into an aggregate of separate symbols.|  
|[get_isStatic](../vs140/IDiaSymbol--get_isStatic.md)|Retrieves a flag indicating whether a function or thunk layer is static.|  
|[get_isStripped](../vs140/IDiaSymbol--get_isStripped.md)|Retrieves a flag indicating whether private symbols have been stripped from the symbol file.|  
|[get_isVirtualInheritance](../vs140/IDiaSymbol--get_isVirtualInheritance.md)|Specifies whether the `this` pointer points to a data member with virtual inheritance.|  
|[IDiaSymbol::get_language](../vs140/IDiaSymbol--get_language.md)|Retrieves the language of the source.|  
|[IDiaSymbol::get_length](../vs140/IDiaSymbol--get_length.md)|Retrieves the number of bytes of memory used by the object represented by this symbol.|  
|[IDiaSymbol::get_lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|Retrieves a reference to the lexical parent of the symbol.|  
|[IDiaSymbol::get_lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|Retrieves the lexical parent identifier of the symbol.|  
|[IDiaSymbol::get_libraryName](../vs140/IDiaSymbol--get_libraryName.md)|Retrieves the file name of the library or object file from which the object was loaded.|  
|[get_liveRangeLength](../vs140/IDiaSymbol--get_liveRangeLength.md)|Returns the length of the address range in which the local symbol is valid.|  
|[get_liveRangeStartAddressSection](../vs140/IDiaSymbol--get_liveRangeStartAddressSection.md)|Returns the section part of the starting address range in which the local symbol is valid.|  
|[get_liveRangeStartAddressOffset](../vs140/IDiaSymbol--get_liveRangeStartAddressOffset.md)|Returns the offset part of the starting address range in which the local symbol is valid.|  
|[get_liveRangeStartRelativeVirtualAddress](../vs140/IDiaSymbol--get_liveRangeStartRelativeVirtualAddress.md)|Returns the start of the address range in which the local symbol is valid.|  
|[IDiaSymbol::get_locationType](../vs140/IDiaSymbol--get_locationType.md)|Retrieves the location type of a data symbol.|  
|[IDiaSymbol::get_lowerBound](../vs140/IDiaSymbol--get_lowerBound.md)|Retrieves the lower bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_lowerBoundId](../vs140/IDiaSymbol--get_lowerBoundId.md)|Retrieves the symbol identifier of the lower bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_machineType](../vs140/IDiaSymbol--get_machineType.md)|Retrieves the type of the target CPU.|  
|[IDiaSymbol::get_managed](../vs140/IDiaSymbol--get_managed.md)|Retrieves a flag that indicating whether the symbol refers to managed code.|  
|[get_memorySpaceKind](../vs140/IDiaSymbol--get_memorySpaceKind.md)|Retrieves the memory space kind.|  
|[IDiaSymbol::get_msil](../vs140/IDiaSymbol--get_msil.md)|Retrieves a flag indicating whether the symbol refers to Microsoft Intermediate Language (MSIL) code.|  
|[IDiaSymbol::get_name](../vs140/IDiaSymbol--get_name.md)|Retrieves the name of the symbol.|  
|[IDiaSymbol::get_nested](../vs140/IDiaSymbol--get_nested.md)|Retrieves a flag indicating whether the user-defined data type is nested.|  
|[get_noInline](../vs140/IDiaSymbol--get_noInline.md)|Retrieves a flag indicating whether the function is marked with the [noinline](../vs140/noinline.md) attribute.|  
|[get_noReturn](../vs140/IDiaSymbol--get_noReturn.md)|Retrieves a flag indicating whether the function has been declared with the [noreturn](../vs140/noreturn.md) attribute.|  
|[get_noStackOrdering](../vs140/IDiaSymbol--get_noStackOrdering.md)|Retrieves a flag indicating whether no stack ordering could be done as part of stack buffer checking.|  
|[get_notReached](../vs140/IDiaSymbol--get_notReached.md)|Retrieves a flag indicating whether the function or label is never reached.|  
|[get_numberOfAcceleratorPointerTags](../vs140/IDiaSymbol--get_numberOfAcceleratorPointerTags.md)|Returns the number of accelerator pointer tags in a C++ AMP stub function.|  
|[get_numberOfModifiers](../vs140/IDiaSymbol--get_numberOfModifiers.md)|Retrieves the number of modifiers that are applied to the original type.|  
|[get_numberOfRegisterIndices](../vs140/IDiaSymbol--get_numberOfRegisterIndices.md)|Retrieves the number of register indices.|  
|[get_numberOfRows](../vs140/IDiaSymbol--get_numberOfRows.md)|Retrieves the number of rows in the matrix.|  
|[get_numberOfColumns](../vs140/IDiaSymbol--get_numberOfColumns.md)|Retrieves the number of columns in the matrix.|  
|[get_objectFileName](../vs140/IDiaSymbol--get_objectFileName.md)|Retrieves the object file name.|  
|[IDiaSymbol::get_objectPointerType](../vs140/IDiaSymbol--get_objectPointerType.md)|Retrieves the type of the object pointer for a class method.|  
|[IDiaSymbol::get_oemId](../vs140/IDiaSymbol--get_oemId.md)|Retrieves the symbol's `oemId` value.|  
|[IDiaSymbol::get_oemSymbolId](../vs140/IDiaSymbol--get_oemSymbolId.md)|Retrieves the symbol's `oemSymbolId` value.|  
|[IDiaSymbol::get_offset](../vs140/IDiaSymbol--get_offset.md)|Retrieves the offset of the symbol location.|  
|[get_optimizedCodeDebugInfo](../vs140/IDiaSymbol--get_optimizedCodeDebugInfo.md)|Retrieves a flag indicating whether the function or label contains optimized code as well as debug information.|  
|[IDiaSymbol::get_overloadedOperator](../vs140/IDiaSymbol--get_overloadedOperator.md)|Retrieves a flag indicating whether the user-defined data type has overloaded operators.|  
|[IDiaSymbol::get_packed](../vs140/IDiaSymbol--get_packed.md)|Retrieves a flag indicating whether the user-defined data type is packed.|  
|[IDiaSymbol::get_platform](../vs140/IDiaSymbol--get_platform.md)|Retrieves the platform type for which the program or compiland was compiled.|  
|[IDiaSymbol::get_pure](../vs140/IDiaSymbol--get_pure.md)|Retrieves a flag that indicating whether the function is pure virtual.|  
|[IDiaSymbol::get_rank](../vs140/IDiaSymbol--get_rank.md)|Retrieves the rank of a FORTRAN multidimensional array.|  
|[IDiaSymbol::get_reference](../vs140/IDiaSymbol--get_reference.md)|Retrieves a flag indicating whether a pointer type is a reference.|  
|[IDiaSymbol::get_registerId](../vs140/IDiaSymbol--get_registerId.md)|Retrieves the register designator of the location.|  
|[get_registerType](../vs140/IDiaSymbol--get_registerType.md)|Retrieves the register type.|  
|[IDiaSymbol::get_relativeVirtualAddress](../vs140/IDiaSymbol--get_relativeVirtualAddress.md)|Retrieves the relative virtual address (RVA) of the location.|  
|[get_restrictedType](../vs140/IDiaSymbol--get_restrictedType.md)|Specifies whether the `this` pointer is flagged as restricted.|  
|[get_samplerSlot](../vs140/IDiaSymbol--get_samplerSlot.md)|Retrieves the sampler slot.|  
|[IDiaSymbol::get_scoped](../vs140/IDiaSymbol--get_scoped.md)|Retrieves a flag indicating whether the user-defined data type appears in a nonglobal lexical scope.|  
|[IDiaSymbol::get_signature](../vs140/IDiaSymbol--get_signature.md)|Retrieves the symbol's signature value.|  
|[get_sizeInUdt](../vs140/IDiaSymbol--get_sizeInUdt.md)|Retrieves the size of a member of a user-defined type.|  
|[IDiaSymbol::get_slot](../vs140/IDiaSymbol--get_slot.md)|Retrieves the slot number of the location.|  
|[IDiaSymbol::get_sourceFileName](../vs140/IDiaSymbol--get_sourceFileName.md)|Retrieves the file name of the source file.|  
|[getSrcLineOnTypeDefn](../vs140/IDiaSymbol--getSrcLineOnTypeDefn.md)|Retrieves the source file and line number that indicate where a specified user-defined type is defined.|  
|[get_stride](../vs140/IDiaSymbol--get_stride.md)|Retrieves the stride of the matrix or strided array.|  
|[get_subType](../vs140/IDiaSymbol--get_subType.md)|Retrieves the sub type.|  
|[get_subTypeId](../vs140/IDiaSymbol--get_subTypeId.md)|Retrieves the sub type ID.|  
|[IDiaSymbol::get_symbolsFileName](../vs140/IDiaSymbol--get_symbolsFileName.md)|Retrieves the name of the file from which the symbols were loaded.|  
|[IDiaSymbol::get_symIndexId](../vs140/IDiaSymbol--get_symIndexId.md)|Retrieves the unique symbol identifier.|  
|[IDiaSymbol::get_symTag](../vs140/IDiaSymbol--get_symTag.md)|Retrieves the symbol type classifier.|  
|[IDiaSymbol::get_targetOffset](../vs140/IDiaSymbol--get_targetOffset.md)|Retrieves the offset section of a thunk target.|  
|[IDiaSymbol::get_targetRelativeVirtualAddress](../vs140/IDiaSymbol--get_targetRelativeVirtualAddress.md)|Retrieves the relative virtual address (RVA) of a thunk target.|  
|[IDiaSymbol::get_targetSection](../vs140/IDiaSymbol--get_targetSection.md)|Retrieves the address section of a thunk target.|  
|[IDiaSymbol::get_targetVirtualAddress](../vs140/IDiaSymbol--get_targetVirtualAddress.md)|Retrieves the virtual address (VA) of a thunk target.|  
|[get_textureSlot](../vs140/IDiaSymbol--get_textureSlot.md)|Retrieves the texture slot.|  
|[IDiaSymbol::get_thisAdjust](../vs140/IDiaSymbol--get_thisAdjust.md)|Retrieves the logical `this` adjustor for the method.|  
|[IDiaSymbol::get_thunkOrdinal](../vs140/IDiaSymbol--get_thunkOrdinal.md)|Retrieves the thunk type of a function.|  
|[IDiaSymbol::get_timeStamp](../vs140/IDiaSymbol--get_timeStamp.md)|Retrieves the timestamp of the underlying executable file.|  
|[IDiaSymbol::get_token](../vs140/IDiaSymbol--get_token.md)|Retrieves the metadata token of a managed function or variable.|  
|[IDiaSymbol::get_type](../vs140/IDiaSymbol--get_type.md)|Retrieves a reference to the function signature.|  
|[IDiaSymbol::get_typeId](../vs140/IDiaSymbol--get_typeId.md)|Retrieves the type identifier of the symbol.|  
|[IDiaSymbol::get_types](../vs140/IDiaSymbol--get_types.md)|Retrieves an array of compiler-specific type values for this symbol.|  
|[IDiaSymbol::get_typeIds](../vs140/IDiaSymbol--get_typeIds.md)|Retrieves an array of compiler-specific type identifier values for this symbol.|  
|[get_uavSlot](../vs140/IDiaSymbol--get_uavSlot.md)|Retrieves the uav slot.|  
|[IDiaSymbol::get_udtKind](../vs140/IDiaSymbol--get_udtKind.md)|Retrieves the variety of a user-defined type (UDT).|  
|[IDiaSymbol::get_unalignedType](../vs140/IDiaSymbol--get_unalignedType.md)|Retrieves a flag indicating whether the user-defined data type is unaligned.|  
|[IDiaSymbol::get_undecoratedName](../vs140/IDiaSymbol--get_undecoratedName.md)|Retrieves the undecorated name for a C++ decorated, or linkage, name.|  
|[IDiaSymbol::get_undecoratedNameEx](../vs140/IDiaSymbol--get_undecoratedNameEx.md)|Extension of the `get_undecoratedName` method that retrieves the undecorated name based on the value of an extension field.|  
|[get_unmodifiedTypeId](../vs140/IDiaSymbol--get_unmodifiedTypeId.md)|Retrieves the ID of the original (unmodified) type.|  
|[IDiaSymbol::get_upperBound](../vs140/IDiaSymbol--get_upperBound.md)|Retrieves the upper bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_upperBoundId](../vs140/IDiaSymbol--get_upperBoundId.md)|Retrieves the symbol identifier of the upper bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_value](../vs140/IDiaSymbol--get_value.md)|Retrieves the value of a constant.|  
|[IDiaSymbol::get_virtual](../vs140/IDiaSymbol--get_virtual.md)|Retrieves a flag indicating whether the function is virtual.|  
|[IDiaSymbol::get_virtualAddress](../vs140/IDiaSymbol--get_virtualAddress.md)|Retrieves the virtual address (VA) of the location.|  
|[IDiaSymbol::get_virtualBaseClass](../vs140/IDiaSymbol--get_virtualBaseClass.md)|Retrieves a flag indicating whether the user-defined data type is a virtual base class.|  
|[IDiaSymbol::get_virtualBaseDispIndex](../vs140/IDiaSymbol--get_virtualBaseDispIndex.md)|Retrieves the index to the virtual base displacement table.|  
|[IDiaSymbol::get_virtualBaseOffset](../vs140/IDiaSymbol--get_virtualBaseOffset.md)|Retrieves the offset in the virtual function table of a virtual function.|  
|[IDiaSymbol::get_virtualBasePointerOffset](../vs140/IDiaSymbol--get_virtualBasePointerOffset.md)|Retrieves the offset of the virtual base pointer.|  
|[get_virtualBaseTableType](../vs140/IDiaSymbol--get_virtualBaseTableType.md)|Retrieves the type of a virtual base table pointer.|  
|[IDiaSymbol::get_virtualTableShape](../vs140/IDiaSymbol--get_virtualTableShape.md)|Retrieves the symbol interface of the type of the virtual table for a user-defined type.|  
|[IDiaSymbol::get_virtualTableShapeId](../vs140/IDiaSymbol--get_virtualTableShapeId.md)|Retrieves the virtual table shape identifier of the symbol.|  
|[IDiaSymbol::get_volatileType](../vs140/IDiaSymbol--get_volatileType.md)|Retrieves a flag indicating whether the user-defined data type is volatile.|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface by calling one of the following methods:  
  
-   [IDiaEnumSymbols::Item](../vs140/IDiaEnumSymbols--Item.md)  
  
-   [IDiaEnumSymbols::Next](../vs140/IDiaEnumSymbols--Next.md)  
  
-   [IDiaEnumSymbolsByAddr::Next](../vs140/IDiaEnumSymbolsByAddr--Next.md)  
  
-   [IDiaEnumSymbolsByAddr::Prev](../vs140/IDiaEnumSymbolsByAddr--Prev.md)  
  
-   [IDiaEnumSymbolsByAddr::symbolByAddr](../vs140/IDiaEnumSymbolsByAddr--symbolByAddr.md)  
  
-   [IDiaEnumSymbolsByAddr::symbolByRVA](../vs140/IDiaEnumSymbolsByAddr--symbolByRVA.md)  
  
-   [IDiaEnumSymbolsByAddr::symbolByVA](../vs140/IDiaEnumSymbolsByAddr--symbolByVA.md)  
  
-   [IDiaSession::findSymbolByAddr](../vs140/IDiaSession--findSymbolByAddr.md)  
  
-   [IDiaSession::findSymbolByRVA](../vs140/IDiaSession--findSymbolByRVA.md)  
  
-   [IDiaSession::findSymbolByRVAEx](../vs140/IDiaSession--findSymbolByRVAEx.md)  
  
-   [IDiaSession::findSymbolByVA](../vs140/IDiaSession--findSymbolByVA.md)  
  
-   [IDiaSession::findSymbolByVAEx](../vs140/IDiaSession--findSymbolByVAEx.md)  
  
-   [IDiaSession::findSymbolByToken](../vs140/IDiaSession--findSymbolByToken.md)  
  
-   [IDiaSession::symbolById](../vs140/IDiaSession--symbolById.md)  
  
-   [IDiaStackWalkHelper::symbolForVA](../vs140/IDiaStackWalkHelper--symbolForVA.md)  
  
-   [IDiaSymbol::get_types](../vs140/IDiaSymbol--get_types.md)  
  
## Example  
 This example shows how to display the local variables for a function at a given relative virtual address. It also shows how symbols of different types are related to each other.  
  
> [!NOTE]
>  `CDiaBSTR` is a class that wraps a `BSTR` and automatically handles freeing the string when the instantiation goes out of scope.  
  
```cpp#  
void DumpLocalVars( DWORD rva, IDiaSession *pSession )  
{  
    CComPtr< IDiaSymbol > pBlock;  
    if ( FAILED( psession->findSymbolByRVA( rva, SymTagBlock, &pBlock ) ) )  
    {  
        Fatal( "Failed to find symbols by RVA" );  
    }  
    CComPtr< IDiaSymbol > pscope;  
    for ( ; pBlock != NULL; )  
    {  
        CComPtr< IDiaEnumSymbols > pEnum;  
        // local data search  
        if ( FAILED( pBlock->findChildren( SymTagNull, NULL, nsNone, &pEnum ) ) )  
        {  
            Fatal( "Local scope findChildren failed" );  
        }  
        CComPtr< IDiaSymbol > pSymbol;  
        DWORD tag;  
        DWORD celt;  
        while ( pEnum != NULL &&  
                SUCCEEDED( pEnum->Next( 1, &pSymbol, &celt ) ) &&  
                celt == 1)  
        {  
            pSymbol->get_symTag( &tag );  
            if ( tag == SymTagData )  
            {  
                CDiaBSTR name;  
                DWORD    kind;  
                pSymbol->get_name( &name );  
                pSymbol->get_dataKind( &kind );  
                if ( name != NULL )  
                    wprintf_s( L"\t%s (%s)\n", name, szDataKinds[ kind ] );  
            }  
            else if ( tag == SymTagAnnotation )  
            {  
                CComPtr< IDiaEnumSymbols > pValues;  
                // local data search  
                wprintf_s( L"\tAnnotation:\n" );  
                if ( FAILED( pSymbol->findChildren( SymTagNull, NULL, nsNone, &pValues ) ) )  
                    Fatal( "Annotation findChildren failed" );  
                pSymbol = NULL;  
                while ( pValues != NULL &&  
                        SUCCEEDED( pValues->Next( 1, &pSymbol, &celt ) ) &&  
                        celt == 1 )  
                {  
                    CComVariant value;  
                    if ( pSymbol->get_value( &value ) != S_OK )  
                        Fatal( "No value for annotation data." );  
                    wprintf_s( L"\t\t%ws\n", value.bstrVal );  
                    pSymbol = NULL;  
                }  
            }  
            pSymbol = NULL;  
        }  
        pBlock->get_symTag( &tag );   
        if ( tag == SymTagFunction )    // stop when at function scope  
            break;  
        // move to lexical parent  
        CComPtr< IDiaSymbol > pParent;  
        if ( SUCCEEDED( pBlock->get_lexicalParent( &pParent ) )  
            && pParent != NULL ) {  
            pBlock = pParent;  
        }  
        else  
        {  
            Fatal( "Finding lexical parent failed." );  
        }  
    };  
}  
```  
  
## Requirements  
 `Header:` Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaEnumSymbolsByAddr](../vs140/IDiaEnumSymbolsByAddr.md)   
 [IDiaEnumSymbols](../vs140/IDiaEnumSymbols.md)   
 [IDiaSession](../vs140/IDiaSession.md)   
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)   
 [Symbols and Symbol Tags](../vs140/Symbols-and-Symbol-Tags.md)   
 [Compiland](../vs140/Compiland.md)