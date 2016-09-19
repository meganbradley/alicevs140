---
title: "IDiaReadExeAtOffsetCallback"
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
ms.assetid: 3c961641-3ce3-4bc3-bd6e-a802fa3bec49
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaReadExeAtOffsetCallback
Enables a client application to supply bytes of an executable file as  specified by file position.  
  
## Syntax  
  
```  
IDiaReadExeAtOffsetCallback : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaReadExeAtOffsetCallback`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaReadExeAtOffsetCallback::ReadExecutableAt](../vs140/IDiaReadExeAtOffsetCallback--ReadExecutableAt.md)|Reads the specified number of bytes starting at the specified offset from an executable file.|  
  
## Remarks  
 The client application implements this interface in order to provide the bytes of the executable using an absolute offset into the executable's file. To use a relative virtual address, implement the [IDiaReadExeAtRVACallback](../vs140/IDiaReadExeAtRVACallback.md) interface.  
  
## Notes for Callers  
 This method is implemented by the client application and passed to the [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md) method as an alternative method for reading the file.  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md)   
 [IDiaReadExeAtRVACallback](../vs140/IDiaReadExeAtRVACallback.md)