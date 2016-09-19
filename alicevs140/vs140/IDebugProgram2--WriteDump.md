---
title: "IDebugProgram2::WriteDump"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 375afb8c-882d-44db-bfa7-e2c9eb555122
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::WriteDump
Writes a dump to a file.  
  
## Syntax  
  
```cpp#  
HRESULT WriteDump(   
   DUMPTYPE  DumpType,  
   LPCOLESTR pszDumpUrl  
);  
```  
  
```c#  
int WriteDump(   
   enum_DUMPTYPE  DumpType,  
   string         pszDumpUrl  
);  
```  
  
#### Parameters  
 `DumpType`  
 [in] A value from the [DUMPTYPE](../vs140/DUMPTYPE.md) enumeration that specifies the type of dump, for example, short or long.  
  
 `pszDumpUrl`  
 [in] The URL to write the dump to. Typically, this is in the form of `file://c:\path\filename.ext`, but may be any valid URL.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 A program dump would typically include the current stack frame, the stack itself, a list of the threads running in the program, and possibly any memory that the program owns.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)