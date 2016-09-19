---
title: "ADDRESS_KIND"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a12fbec-7088-4cf9-8f6f-ad8ddec6009a
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# ADDRESS_KIND
Specifies the kinds of addresses.  
  
## Syntax  
  
```cpp  
enum enum_ADDRESS_KIND {  
   ADDRESS_KIND_NATIVE                  = 0x0001,  
   ADDRESS_KIND_UNMANAGED_THIS_RELATIVE = 0x0002,  
   ADDRESS_KIND_UNMANAGED_PHYSICAL      = 0x0005,  
   ADDRESS_KIND_METADATA_METHOD         = 0x0010,  
   ADDRESS_KIND_METADATA_FIELD          = 0x0011,  
   ADDRESS_KIND_METADATA_LOCAL          = 0x0012,  
   ADDRESS_KIND_METADATA_PARAM          = 0x0013,  
   ADDRESS_KIND_METADATA_ARRAYELEM      = 0x0014,  
   ADDRESS_KIND_METADATA_RETVAL         = 0x0015,  
};  
typedef DWORD ADDRESS_KIND;  
```  
  
```c#  
public enum enum_ADDRESS_KIND {  
   ADDRESS_KIND_NATIVE                  = 0x0001,  
   ADDRESS_KIND_UNMANAGED_THIS_RELATIVE = 0x0002,  
   ADDRESS_KIND_UNMANAGED_PHYSICAL      = 0x0005,  
   ADDRESS_KIND_METADATA_METHOD         = 0x0010,  
   ADDRESS_KIND_METADATA_FIELD          = 0x0011,  
   ADDRESS_KIND_METADATA_LOCAL          = 0x0012,  
   ADDRESS_KIND_METADATA_PARAM          = 0x0013,  
   ADDRESS_KIND_METADATA_ARRAYELEM      = 0x0014,  
   ADDRESS_KIND_METADATA_RETVAL         = 0x0015,  
};  
```  
  
## Terms  
 ADDRESS_KIND_NATIVE  
 A native address, represented by the [NATIVE_ADDRESS](../vs140/NATIVE_ADDRESS.md) structure.  
  
 ADDRESS_KIND_UNMANAGED_THIS_RELATIVE  
 An unmanaged address relative to a `this` (`Me` in Visual Basic) pointer and represented by the [UNMANAGED_ADDRESS_THIS_RELATIVE](../vs140/UNMANAGED_ADDRESS_THIS_RELATIVE.md) structure.  
  
 ADDRESS_KIND_UNMANAGED_PHYSICAL  
 An unmanaged physical address, represented by the [UNMANAGED_ADDRESS_PHYSICAL](../vs140/UNMANAGED_ADDRESS_PHYSICAL.md) structure.  
  
 ADDRESS_KIND_METHOD  
 A method of a class, represented by the [METADATA_ADDRESS_METHOD](../vs140/METADATA_ADDRESS_METHOD.md) structure.  
  
 ADDRESS_KIND_FIELD  
 A field of a class, represented by the [METADATA_ADDRESS_FIELD](../vs140/METADATA_ADDRESS_FIELD.md) structure.  
  
 ADDRESS_KIND_LOCAL  
 The address is for a local variable and is represented by the [METADATA_ADDRESS_LOCAL](../vs140/METADATA_ADDRESS_LOCAL.md) structure.  
  
 ADDRESS_KIND_PARAM  
 A method or function parameter, represented by the [METADATA_ADDRESS_PARAM](../vs140/METADATA_ADDRESS_PARAM.md) structure.  
  
 ADDRESS_KIND_ARRAYELEM  
 An array element, represented by the [METADATA_ADDRESS_ARRAYELEM](../vs140/METADATA_ADDRESS_ARRAYELEM.md) structure.  
  
 ADDRESS_KIND_RETVAL  
 A return value, represented by the [METADATA_ADDRESS_RETVAL](../vs140/METADATA_ADDRESS_RETVAL.md) structure.  
  
## Remarks  
 The [IDebugAddress::GetAddress](../vs140/IDebugAddress--GetAddress.md) method returns the [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md) structure which contains a union of possible structures, the [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md) structure. The `dwKind` field of the `DEBUG_ADDRESS_UNION` structure holds the `ADDRESS_KIND` value and describes how to interpret the union field.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [IDebugAddress::GetAddress](../vs140/IDebugAddress--GetAddress.md)   
 [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md)   
 [DEBUG_ADDRESS_UNION](../vs140/DEBUG_ADDRESS_UNION.md)