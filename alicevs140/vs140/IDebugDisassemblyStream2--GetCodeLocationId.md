---
title: "IDebugDisassemblyStream2::GetCodeLocationId"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 567adfb8-2f54-499a-a027-e4ecb82277ef
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDisassemblyStream2::GetCodeLocationId
Returns a code location identifier for a particular code context.  
  
## Syntax  
  
```cpp#  
HRESULT GetCodeLocationId(   
   IDebugCodeContext2* pCodeContext,  
   UINT64*             puCodeLocationId  
);  
```  
  
```c#  
int GetCodeLocationId(   
   IDebugCodeContext2 pCodeContext,  
   out ulong          puCodeLocationId  
);  
```  
  
#### Parameters  
 `pCodeContext`  
 [in] An [IDebugCodeContext2](../vs140/IDebugCodeContext2.md) object to be converted to an identifier.  
  
 `puCodeLocationId`  
 [out] Returns the code location identifier. See Remarks.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_CODE_CONTEXT_OUT_OF_SCOPE` if the code context is valid but outside the scope.  
  
## Remarks  
 The code location identifier is specific to the debug engine (DE) supporting the disassembly. This location identifier is used internally by the DE to track positions in the code and is typically an address or offset of some kind. The only requirement is that if the code context of one location is less than the code context of another location, then the corresponding code location identifier of the first code context must also be less than the code location identifier of the second code context.  
  
 To retrieve the code context of a code location identifier, call the [IDebugDisassemblyStream2::GetCodeContext](../vs140/IDebugDisassemblyStream2--GetCodeContext.md) method.  
  
## See Also  
 [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md)   
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)   
 [IDebugDisassemblyStream2::GetCodeContext](../vs140/IDebugDisassemblyStream2--GetCodeContext.md)