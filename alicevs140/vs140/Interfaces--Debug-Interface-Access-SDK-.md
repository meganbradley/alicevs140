---
title: "Interfaces (Debug Interface Access SDK)"
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
ms.assetid: 62aee7c3-d314-4272-a32b-b2818f32fab8
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Interfaces (Debug Interface Access SDK)
Methods are listed alphabetically under each interface in the table of contents and on the interface page in Vtable order.  
  
## In This Section  
 [IDiaAddressMap](../vs140/IDiaAddressMap.md)  
 Provides control over how the DIA SDK computes virtual and relative virtual addresses for debug objects.  
  
 [IDiaDataSource](../vs140/IDiaDataSource.md)  
 Initiates access to a source of debugging symbols.  
  
 [IDiaEnumDebugStreamData](../vs140/IDiaEnumDebugStreamData.md)  
 Provides access to the records in a debug data stream.  
  
 [IDiaEnumDebugStreams](../vs140/IDiaEnumDebugStreams.md)  
 Enumerates the various debug streams contained in the data source.  
  
 [IDiaEnumFrameData](../vs140/IDiaEnumFrameData.md)  
 Enumerates the various frame data elements contained in the data source.  
  
 [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md)  
 Enumerate the various injected sources contained in the data source.  
  
 [IDiaEnumLineNumbers](../vs140/IDiaEnumLineNumbers.md)  
 Enumerates the various line numbers contained in the data source.  
  
 [IDiaEnumSectionContribs](../vs140/IDiaEnumSectionContribs.md)  
 Enumerates the various section contributions contained in the data source.  
  
 [IDiaEnumSegments](../vs140/IDiaEnumSegments.md)  
 Enumerates the various segments contained in the data source.  
  
 [IDiaEnumSourceFiles](../vs140/IDiaEnumSourceFiles.md)  
 Enumerates the various source files contained in the data source.  
  
 [IDiaEnumStackFrames](../vs140/IDiaEnumStackFrames.md)  
 Enumerates the various stack frames available.  
  
 [IDiaEnumSymbols](../vs140/IDiaEnumSymbols.md)  
 Enumerates the various symbols contained in the data source.  
  
 [IDiaEnumSymbolsByAddr](../vs140/IDiaEnumSymbolsByAddr.md)  
 Enumerates by address the various symbols contained in the data source.  
  
 [IDiaEnumTables](../vs140/IDiaEnumTables.md)  
 Enumerates the various tables contained in the data source.  
  
 [IDiaFrameData](../vs140/IDiaFrameData.md)  
 Exposes the details of a stack frame.  
  
 [IDiaImageData](../vs140/IDiaImageData.md)  
 Exposes the details of the base location and memory offsets of the module or image.  
  
 [IDiaInjectedSource](../vs140/IDiaInjectedSource.md)  
 Accesses the program source code stored in the DIA data source.  
  
 [IDiaLineNumber](../vs140/IDiaLineNumber.md)  
 Accesses information that describes the process of mapping from a block of bytes of image text to a source file line number.  
  
 [IDiaLoadCallback](../vs140/IDiaLoadCallback.md)  
 Receives callbacks from the DIA symbol locating procedure, thus enabling a user interface to report on the progress of the location attempt.  
  
 [IDiaLoadCallback2](../vs140/IDiaLoadCallback2.md)  
 Receives callbacks from the DIA symbol locating procedure, allowing restrictions to be imposed on the locating process.  
  
 [IDiaPropertyStorage](../vs140/IDiaPropertyStorage.md)  
 Allows you to read the persistent properties of a DIA property set.  
  
 [IDiaReadExeAtRVACallback](../vs140/IDiaReadExeAtRVACallback.md)  
 Enables a client application to supply bytes of an executable file as specified by file position.  
  
 [IDiaReadExeAtOffsetCallback](../vs140/IDiaReadExeAtOffsetCallback.md)  
 Enables a client application to supply bytes of an executable file as specified by a relative virtual address.  
  
 [IDiaSectionContrib](../vs140/IDiaSectionContrib.md)  
 Retrieves data describing a section contribution, that is, a contiguous block of memory contributed to the image by a compiland.  
  
 [IDiaSegment](../vs140/IDiaSegment.md)  
 Maps data from the section number to segments of address space.  
  
 [IDiaSession](../vs140/IDiaSession.md)  
 Provides a query context for debug symbols.  
  
 [IDiaSourceFile](../vs140/IDiaSourceFile.md)  
 Represents a source file.  
  
 [IDiaStackFrame](../vs140/IDiaStackFrame.md)  
 Exposes the properties of a stack frame.  
  
 [IDiaStackWalker](../vs140/IDiaStackWalker.md)  
 Provides methods to do a stack walk using the PDB file.  
  
 [IDiaStackWalkFrame](../vs140/IDiaStackWalkFrame.md)  
 Maintains stack context between invocations of the [IDiaFrameData::execute](../vs140/IDiaFrameData--execute.md) method.  
  
 [IDiaStackWalkHelper](../vs140/IDiaStackWalkHelper.md)  
 Facilitates walking the stack using the program debug database (PDB) file.  
  
 [IDiaSymbol](../vs140/IDiaSymbol.md)  
 Describes the properties of a symbol instance.  
  
 [IDiaTable](../vs140/IDiaTable.md)  
 Enumerates a DIA data source table.  
  
## Related Sections  
 [Enumerations and Structures](../vs140/Enumerations-and-Structures.md)  
 Describes the enumerations and structures used by the various interfaces of the DIA SDK.  
  
 [Constants (Debug Interface Access SDK)](../vs140/Constants--Debug-Interface-Access-SDK-.md)  
 Describes the constants available in the DIA SDK.  
  
## See Also  
 [Reference](../vs140/Debug-Interface-Access-SDK-Reference.md)