---
title: "IDiaStackFrame::get_rawLVarInstanceValue"
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
ms.assetid: ce526259-85a6-475b-9274-0b3a21d95db2
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackFrame::get_rawLVarInstanceValue
This method retrieves the value of the specified local variable as raw bytes.  
  
## Syntax  
  
```cpp#  
HRESULT get_rawLVarInstanceValue(  
   IDiaLVarInstance* pInstance,  
   DWORD             cbDataMax,  
   DWORD*            pcbData,  
   BYTE*             pbData  
);  
```  
  
#### Parameters  
 `pInstance`  
 [in] An `IDiaLVarInstance` object representing an instance of local variable to get the value for.  
  
 `cbDataMax`  
 [in] Maximum number of bytes in the buffer pointed to by `pbData`. This can be a maximum of 8 bytes (`sizeof(ULONGLONG)`).  
  
 `pcbData`  
 [out] Returns the actual number of bytes stored in the buffer.  
  
 `pbData`  
 [out] A buffer to be filled in with data. This cannot be `NULL`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaStackFrame](../vs140/IDiaStackFrame.md)