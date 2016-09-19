---
title: "BSTR_ARRAY"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 48da37f7-a237-48a9-9ff9-389c1a00862c
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BSTR_ARRAY
A structure that describes an array of strings.  
  
## Syntax  
  
```cpp#  
typedef struct tagBSTR_ARRAY {  
   DWORD dwCount;  
   BSTR* Members;  
} BSTR_ARRAY;  
```  
  
```c#  
struct BSTR_ARRAY {  
   DWORD    dwCount;  
   string[] Members;  
}  
```  
  
## Terms  
 dwCount  
 Number of strings in `Members` array.  
  
 Members  
 Array of strings.  
  
## Remarks  
 This structure is returned from the [IDebugPortSupplier3::EnumPersistedPorts](../vs140/IDebugPortSupplier3--EnumPersistedPorts.md) method.  
  
 [C++ only] Each individual string must be freed using `SysFreeString`, and the `Members` array must be freed with `CoTaskMemFree`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [IDebugPortSupplier3::EnumPersistedPorts](../vs140/IDebugPortSupplier3--EnumPersistedPorts.md)