---
title: "SEEK_START"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 55bd8901-626e-428b-a263-23b14417f4c6
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# SEEK_START
Specifies the position from which to start seeking in a disassembly stream.  
  
## Syntax  
  
```cpp#  
enum enum_SEEK_START {   
   SEEK_START_BEGIN       = 0x0001,  
   SEEK_START_END         = 0x0002,  
   SEEK_START_CURRENT     = 0x0003,  
   SEEK_START_CODECONTEXT = 0x0004,  
   SEEK_START_CODELOCID   = 0x0005  
};  
typedef DWORD SEEK_START;  
```  
  
```c#  
public enum enum_SEEK_START {   
   SEEK_START_BEGIN       = 0x0001,  
   SEEK_START_END         = 0x0002,  
   SEEK_START_CURRENT     = 0x0003,  
   SEEK_START_CODECONTEXT = 0x0004,  
   SEEK_START_CODELOCID   = 0x0005  
};  
```  
  
## Members  
 SEEK_START_BEGIN  
 Starts seeking at the beginning of the current document.  
  
 SEEK_START_END  
 Starts seeking at the end of the current document.  
  
 SEEK_START_CURRENT  
 Starts seeking at the current position of the current document.  
  
 SEEK_START_CODECONTEXT  
 Starts seeking at the given code context of the current document.  
  
 SEEK_START_CODELOCID  
 Starts seeking at the given code location identifier. Code location identifiers are obtained by calling [GetCurrentLocation](../vs140/IDebugDisassemblyStream2--GetCurrentLocation.md).  
  
## Remarks  
 Passed as an argument to the [Seek](../vs140/IDebugDisassemblyStream2--Seek.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [Seek](../vs140/IDebugDisassemblyStream2--Seek.md)   
 [GetCurrentLocation](../vs140/IDebugDisassemblyStream2--GetCurrentLocation.md)