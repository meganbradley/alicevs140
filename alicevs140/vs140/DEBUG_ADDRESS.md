---
title: "DEBUG_ADDRESS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 79f5e765-9aac-4b6e-82ef-bed88095e9ba
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# DEBUG_ADDRESS
This structure represents an address.  
  
## Syntax  
  
```cpp  
typedef struct _tagDEBUG_ADDRESS {  
   ULONG32             ulAppDomainID;  
   GUID                guidModule;  
   _mdToken            tokClass;  
   DEBUG_ADDRESS_UNION addr;  
} DEBUG_ADDRESS;  
```  
  
```c#  
public struct DEBUG_ADDRESS {  
   public uint                ulAppDomainID;  
   public Guid                guidModule;  
   public int                 tokClass;  
   public DEBUG_ADDRESS_UNION addr;  
}  
```  
  
## Terms  
 ulAppDomainID  
 The process ID.  
  
 guidModule  
 The GUID of the module that contains this address.  
  
 tokClass  
 The token identifying the class or type of this address.  
  
> [!NOTE]
>  This value is specific to a symbol provider and therefore has no general meaning other than as an identifier for a class type.  
  
 addr  
 A [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md) structure, which contains a union of structures that describe the individual address types. The value `addr`.`dwKind` comes from the [ADDRESS_KIND](../vs140/ADDRESS_KIND.md) enumeration, which explains how to interpret the union.  
  
## Remarks  
 This structure is passed to the [IDebugAddress::GetAddress](../vs140/IDebugAddress--GetAddress.md) method to be filled in.  
  
 **Warning [C++ only]**  
  
 If `addr.dwKind` is `ADDRESS_KIND_METADATA_LOCAL` and if `addr.addr.addrLocal.pLocal` is not a null value, then you must call `Release` on the token pointer:  
  
```  
if (addr.dwKind == ADDRESS_KIND_METADATA_LOCAL &&  addr.addr.addrLocal.pLocal != NULL)  
{  
    addr.addr.addrLocal.pLocal->Release();  
}  
```  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [IDebugAddress::GetAddress](../vs140/IDebugAddress--GetAddress.md)   
 [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md)   
 [ADDRESS_KIND](../vs140/ADDRESS_KIND.md)