---
title: "UNMANAGED_ADDRESS_PHYSICAL"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fed09686-caa6-4efc-851e-a0432019e9d0
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# UNMANAGED_ADDRESS_PHYSICAL
This structure represents a physical address.  
  
## Syntax  
  
```cpp  
typedef struct _tagUNMANAGED_ADDRESS_PHYSICAL {  
   ULONGLONG offset;  
} UNMANAGED_ADDRESS_PHYSICAL;  
```  
  
```c#  
public struct UNMANAGED_ADDRESS_PHYSICAL {  
   public ulong offset;  
}  
```  
  
## Terms  
 offset  
 A 64-bit offset into a physical address space.  
  
## Remarks  
 This structure is part of the union in the [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md) structure when the `dwKind` field of the `DEBUG_ADDRESS_UNION` structure is set to `ADDRESS_KIND_UNMANAGED_PHYSICAL` (a value from the [ADDRESS_KIND](../vs140/ADDRESS_KIND.md) enumeration).  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md)