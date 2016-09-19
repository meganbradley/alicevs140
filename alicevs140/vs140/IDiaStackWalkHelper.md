---
title: "IDiaStackWalkHelper"
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
ms.assetid: d66e5c84-565d-494e-8486-f91db9a34548
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackWalkHelper
Facilitates walking the stack using the program debug database (.pdb) file.  
  
## Syntax  
  
```  
  
IDiaStackWalkHelper: IUnknown  
  
```  
  
## Methods in VTable Order  
 The table below shows the methods of `IDiaStackWalkHelper`:  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaStackWalkHelper::get_registerValue](../vs140/IDiaStackWalkHelper--get_registerValue.md)|Retrieves the value of a register.|  
|[IDiaStackWalkHelper::put_registerValue](../vs140/IDiaStackWalkHelper--put_registerValue.md)|Sets the value of a register.|  
|[IDiaStackWalkHelper::readMemory](../vs140/IDiaStackWalkHelper--readMemory.md)|Reads a block of data from the executable's image in memory.|  
|[IDiaStackWalkHelper::searchForReturnAddress](../vs140/IDiaStackWalkHelper--searchForReturnAddress.md)|Searches the specified stack frame for the nearest function return address.|  
|[IDiaStackWalkHelper::searchForReturnAddressStart](../vs140/IDiaStackWalkHelper--searchForReturnAddressStart.md)|Searches the specified stack frame for a return address at or near the specified stack address.|  
|[IDiaStackWalkHelper::frameForVA](../vs140/IDiaStackWalkHelper--frameForVA.md)|Retrieves the stack frame that contains the specified virtual address.|  
|[IDiaStackWalkHelper::symbolForVA](../vs140/IDiaStackWalkHelper--symbolForVA.md)|Retrieves the symbol that contains the specified virtual address. **Note:**  Symbol must have the type `SymTagFunctionType` (a value from the [SymTagEnum](../vs140/SymTagEnum.md) enumeration).|  
|[pdataForVA](../vs140/IDiaStackWalkHelper--pdataForVA.md)|Returns the PDATA data block  associated with the specified virtual address.|  
|[IDiaStackWalkHelper::imageForVA](../vs140/IDiaStackWalkHelper--imageForVA.md)|Retrieves the starting virtual address of an executable, given a virtual address somewhere in the executable's memory space.|  
  
## Remarks  
 This interface is called by the DIA code to obtain information about the executable to construct a list of stack frames during program execution.  
  
## Notes for Callers  
 A client application implements this interface to support walking the stack during program execution. An instance of this interface is passed to the [IDiaStackWalker::getEnumFrames](../vs140/IDiaStackWalker--getEnumFrames.md) or [IDiaStackWalker::getEnumFrames2](../vs140/IDiaStackWalker--getEnumFrames2.md) methods.  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaFrameData](../vs140/IDiaFrameData.md)   
 [SymTagEnum Enumeration](../vs140/SymTagEnum.md)   
 [IDiaStackWalker::getEnumFrames](../vs140/IDiaStackWalker--getEnumFrames.md)   
 [IDiaStackWalker::getEnumFrames2](../vs140/IDiaStackWalker--getEnumFrames2.md)