---
title: "dwTYPE_KIND"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6ff56b0f-c502-4e6c-9829-bfa05361b783
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# dwTYPE_KIND
Specifies how to interpret the type of an [IDebugField](../vs140/IDebugField.md) object.  
  
## Syntax  
  
```cpp#  
enum enum_dwTYPE_KIND {  
   TYPE_KIND_METADATA = 0x0001,  
   TYPE_KIND_PDB      = 0x0002,  
   TYPE_KIND_BUILT    = 0x0003,  
};  
  
typedef DWORD dwTYPE_KIND;  
```  
  
```c#  
public enum enum_dwTYPE_KIND {  
   TYPE_KIND_METADATA = 0x0001,  
   TYPE_KIND_PDB      = 0x0002,  
   TYPE_KIND_BUILT    = 0x0003,  
};  
```  
  
#### Parameters  
 TYPE_KIND_METADATA  
 The [TYPE_INFO](../vs140/TYPE_INFO.md) union should be interpreted as a [METADATA_TYPE](../vs140/METADATA_TYPE.md) structure.  
  
 TYPE_KIND_PDB  
 The `TYPE_INFO` union should be interpreted as a [PDB_TYPE](../vs140/PDB_TYPE.md) structure.  
  
 TYPE_KIND_BUILT  
 The `TYPE_INFO` union should be interpreted as a [BUILT_TYPE](../vs140/BUILT_TYPE.md) structure.  
  
## Remarks  
 The values of this enumeration appear in the `dwKind` field of the [TYPE_INFO](../vs140/TYPE_INFO.md) structure and are used to determine how to interpret the `type` union member. The `TYPE_INFO` structure is returned by a call to the [IDebugField::GetTypeInfo](../vs140/IDebugField--GetTypeInfo.md) method.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [TYPE_INFO](../vs140/TYPE_INFO.md)   
 [IDebugField::GetTypeInfo](../vs140/IDebugField--GetTypeInfo.md)   
 [METADATA_TYPE](../vs140/METADATA_TYPE.md)   
 [PDB_TYPE](../vs140/PDB_TYPE.md)   
 [BUILT_TYPE](../vs140/BUILT_TYPE.md)