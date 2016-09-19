---
title: "METADATA_ADDRESS_METHOD"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc0e5370-1b4f-4867-837f-0d63c4b9dd09
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# METADATA_ADDRESS_METHOD
This structure represents the address of a method of a class.  
  
## Syntax  
  
```cpp  
typedef struct _tagMETADATA_ADDRESS_METHOD {  
   _mdToken tokMethod;  
   DWORD    dwOffset;  
   DWORD    dwVersion;  
} METADATA_ADDRESS_METHOD;  
```  
  
```c#  
public struct METADATA_ADDRESS_METHOD {  
   public int  tokMethod;  
   public uint dwOffset;  
   public uint dwVersion;  
}  
```  
  
## Terms  
 tokMethod  
 The ID of the method.  
  
 [C++] `_mdToken` is a `typedef` for a 32-bit `int`.  
  
 dwOffset  
 The offset from the class start to this method (can represent the offset into the vtable).  
  
 dwVersion  
 The version of the method (this value is unique to the symbol provider).  
  
## Remarks  
 This structure is part of the union in the [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md) structure when the `dwKind` field of the `DEBUG_ADDRESS_UNION` structure is set to `ADDRESS_KIND_METHOD` (a value from the [ADDRESS_KIND](../vs140/ADDRESS_KIND.md) enumeration).  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md)   
 [ADDRESS_KIND](../vs140/ADDRESS_KIND.md)