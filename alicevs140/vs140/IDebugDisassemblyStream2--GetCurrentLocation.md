---
title: "IDebugDisassemblyStream2::GetCurrentLocation"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 512302f1-12b1-4107-8a6e-c5bc878ce1c3
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDisassemblyStream2::GetCurrentLocation
Returns a code location identifier that represents the current code location.  
  
## Syntax  
  
```cpp#  
HRESULT GetCurrentLocation(   
   UINT64* puCodeLocationId  
);  
```  
  
```c#  
int GetCurrentLocation(   
   out ulong puCodeLocationId  
);  
```  
  
#### Parameters  
 `puCodeLocationId`  
 [out] Returns the code location identifier. See the Remarks section for the [IDebugDisassemblyStream2::GetCodeLocationId](../vs140/IDebugDisassemblyStream2--GetCodeLocationId.md) method for a description of a code location identifier.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The code location identifier can be converted to a code context by calling the [GetCodeContext](../vs140/IDebugDisassemblyStream2--GetCodeContext.md) method.  
  
## See Also  
 [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md)   
 [IDebugDisassemblyStream2::GetCodeLocationId](../vs140/IDebugDisassemblyStream2--GetCodeLocationId.md)   
 [GetCodeContext](../vs140/IDebugDisassemblyStream2--GetCodeContext.md)