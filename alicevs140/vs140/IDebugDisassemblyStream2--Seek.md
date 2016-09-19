---
title: "IDebugDisassemblyStream2::Seek"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: afec3008-b1e0-4803-ad24-195dbfb6497e
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDisassemblyStream2::Seek
Moves the read pointer in the disassembly stream a given number of instructions relative to a specified position.  
  
## Syntax  
  
```cpp#  
HRESULT Seek(   
   SEEK_START          dwSeekStart,  
   IDebugCodeContext2* pCodeContext,  
   UINT64              uCodeLocationId,  
   INT64               iInstructions  
);  
```  
  
```c#  
int Seek(   
   enum_SEEK_START    dwSeekStart,  
   IDebugCodeContext2 pCodeContext,  
   ulong              uCodeLocationId,  
   long               iInstructions  
);  
```  
  
#### Parameters  
 `dwSeekStart`  
 [in] A value from the [SEEK_START](../vs140/SEEK_START.md) enumeration that specifies the relative position to begin the seek process.  
  
 `pCodeContext`  
 [in] The [IDebugCodeContext2](../vs140/IDebugCodeContext2.md) object representing the code context that the seek operation is relative to. This parameter is used only if `dwSeekStart` = `SEEK_START_CODECONTEXT`; otherwise, this parameter is ignored and can be a null value.  
  
 `uCodeLocationId`  
 [in] The code location identifier that the seek operation is relative to. This parameter is used if `dwSeekStart` = `SEEK_START_CODELOCID`; otherwise, this parameter is ignored and can be set to 0. See the Remarks section for the [IDebugDisassemblyStream2::GetCodeLocationId](../vs140/IDebugDisassemblyStream2--GetCodeLocationId.md) method for a description of a code location identifier.  
  
 `iInstructions`  
 [in] The number of instructions to move relative to the position specified in `dwSeekStart`. This value can be negative to move backwards.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if the seek position was to a point beyond the list of available instructions. Otherwise, returns an error code.  
  
## Remarks  
 If the seek was to a position before the beginning of the list, the read position is set to the first instruction in the list. If the see was to a position after the end of the list, the read position is set to the last instruction in the list.  
  
## See Also  
 [IDebugDisassemblyStream2](../vs140/IDebugDisassemblyStream2.md)   
 [SEEK_START](../vs140/SEEK_START.md)   
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)   
 [IDebugDisassemblyStream2::GetCodeLocationId](../vs140/IDebugDisassemblyStream2--GetCodeLocationId.md)