---
title: "IDiaReadExeAtRVACallback"
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
ms.assetid: b2892513-3952-4f99-9b98-60cb9b1fdc91
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaReadExeAtRVACallback
Enables a client application to supply bytes of an executable file as specified by a relative virtual address.  
  
## Syntax  
  
```  
IDiaReadExeAtRVACallback : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaReadExeAtRVACallback`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaReadExeAtRVACallback::ReadExecutableAtRVA](../vs140/IDiaReadExeAtRVACallback--ReadExecutableAtRVA.md)|Reads the specified number of bytes starting at the specified relative virtual address (RVA) from the executable file.|  
  
## Remarks  
 The client application implements this interface in order to provide the bytes of the executable using a relative virtual address into the executable's file. To use an absolute file offset, implement the [IDiaReadExeAtOffsetCallback](../vs140/IDiaReadExeAtOffsetCallback.md) interface.  
  
## Notes for Callers  
 This method is implemented by the client application and passed to the [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md) method as an alternative method for reading the file.  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md)   
 [IDiaReadExeAtOffsetCallback](../vs140/IDiaReadExeAtOffsetCallback.md)