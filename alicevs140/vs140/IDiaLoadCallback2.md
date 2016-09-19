---
title: "IDiaLoadCallback2"
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
ms.assetid: 9a44277d-cbed-4811-9bad-5a2aa0f09323
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaLoadCallback2
Receives callbacks from the DIA symbol locating procedure, allowing restrictions to be imposed on the locating process.  
  
## Syntax  
  
```  
IDiaLoadCallback2 : IDiaLoadCallback  
```  
  
## Methods in Vtable Order  
 In addition to the methods in the [IDiaLoadCallback](../vs140/IDiaLoadCallback.md) interface, this interface exposes the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaLoadCallback2::RestrictOriginalPathAccess](../vs140/IDiaLoadCallback2--RestrictOriginalPathAccess.md)|Determines if looking for a .pdb file in the original debug directory.|  
|[IDiaLoadCallback2::RestrictReferencePathAccess](../vs140/IDiaLoadCallback2--RestrictReferencePathAccess.md)|Determines if looking for a .pdb file is allowed in the path where the .exe file is located.|  
|[IDiaLoadCallback2::RestrictDBGAccess](../vs140/IDiaLoadCallback2--RestrictDBGAccess.md)|Determines if looking for debug information is allowed from .dbg files.|  
|[RestrictSystemRootAccess](../vs140/IDiaLoadCallback2--RestrictSystemRootAccess.md)|Determines if searching for .pdb files is allowed in the system root directory.|  
  
## Remarks  
 The client application implements this interface and provides a reference to it in the call to the [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md) method. Remember to implement all of the methods in the [IDiaLoadCallback](../vs140/IDiaLoadCallback.md) interface as well.  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md)   
 [IDiaReadExeAtOffsetCallback](../vs140/IDiaReadExeAtOffsetCallback.md)   
 [IDiaReadExeAtRVACallback](../vs140/IDiaReadExeAtRVACallback.md)   
 [IDiaLoadCallback](../vs140/IDiaLoadCallback.md)