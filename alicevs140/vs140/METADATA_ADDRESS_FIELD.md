---
title: "METADATA_ADDRESS_FIELD"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 15ab45fe-6b3b-4e09-880b-31b34f523607
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# METADATA_ADDRESS_FIELD
This structure represents the address of a field of a class or structure.  
  
## Syntax  
  
```cpp  
typedef struct _tagMETADATA_ADDRESS_FIELD {  
   _mdToken tokField;  
} METADATA_ADDRESS_FIELD  
```  
  
```c#  
public struct METADATA_ADDRESS_FIELD {  
   public int tokField;  
}  
```  
  
## Terms  
 tokField  
 The ID of the field token.  
  
 [C++] `_mdToken` is a `typedef` for a 32-bit `int`.  
  
## Remarks  
 This structure is part of the union in the [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md) structure when the `dwKind` field of the `DEBUG_ADDRESS_UNION` structure is set to `ADDRESS_KIND_FIELD` (a value from the [ADDRESS_KIND](../vs140/ADDRESS_KIND.md) enumeration).  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md)   
 [ADDRESS_KIND](../vs140/ADDRESS_KIND.md)