---
title: "METADATA_ADDRESS_RETVAL"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5b0ec0fb-84b3-4ce7-8e24-becf3d881d7d
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# METADATA_ADDRESS_RETVAL
This structure represents a return value from a method or function.  
  
## Syntax  
  
```cpp  
typedef struct _tagMETADATA_ADDRESS_RETVAL {  
   _mdToken tokMethod;  
   DWORD    dwCorType;  
   DWORD    dwSigSize;  
   BYTE     rgSig[10];  
} METADATA_ADDRESS_RETVAL;  
```  
  
```c#  
public struct METADATA_ADDRESS_RETVAL {  
   public int    tokMethod;  
   public uint   dwCorType;  
   public uint   dwSigSize;  
   public byte[] rgSig;  
}  
```  
  
## Terms  
 tokMethod  
 The ID of the method this return value is for.  
  
 dwCorType  
 The base type of return value. This is a value from the `CorElementType` enumeration defined in the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] SDK corhdr.h file.  
  
 dwSigSize  
 The size of the return value signature (as stored in `rgSig`).  
  
 rgSig  
 An array of bytes forming the signature of the return value.  
  
## Remarks  
 This structure is part of the union in the [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md) structure when the `dwKind` field of the `DEBUG_ADDRESS_UNION` structure is set to `ADDRESS_KIND_RETVAL` (a value from the [ADDRESS_KIND](../vs140/ADDRESS_KIND.md) enumeration).  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md)   
 [ADDRESS_KIND](../vs140/ADDRESS_KIND.md)