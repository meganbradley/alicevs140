---
title: "DEBUG_REFERENCE_INFO"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 24b83d00-d756-42a1-8083-730f998761dc
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# DEBUG_REFERENCE_INFO
Describes a reference.  
  
## Syntax  
  
```cpp#  
typedef struct tagDEBUG_REFERENCE_INFO {   
   DEBUGREF_INFO_FLAGS dwFields;  
   BSTR                bstrName;  
   BSTR                bstrType;  
   BSTR                bstrValue;  
   DBG_ATTRIB_FLAGS    dwAttrib;  
   REFERENCE_TYPE.     dwRefType;  
   IDebugReference2*   m_pReference;  
} DEBUG_REFERENCE_INFO;  
```  
  
```c#  
public struct DEBUG_REFERENCE_INFO {   
   public uint             dwFields;  
   public string           bstrName;  
   public string           bstrType;  
   public string           bstrValue;  
   public ulong            dwAttrib;  
   public uint.            dwRefType;  
   public IDebugReference2 m_pReference;  
};  
```  
  
## Members  
 dwFields  
 A combination of flags from the [DEBUGREF_INFO_FLAGS](../vs140/DEBUGREF_INFO_FLAGS.md) enumeration that specifies which fields are filled out.  
  
 bstrName  
 The user-specified name of the [IDebugReference2](../vs140/IDebugReference2.md) object.  
  
 bstrType  
 The reference type as a formatted string.  
  
 bstrValue  
 The reference value as a formatted string  
  
 dwAttrib  
 A combination of flags from the [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md) enumeration that specifies the flags for the debug property attributes.  
  
 dwRefType  
 A value from the [REFERENCE_TYPE](../vs140/REFERENCE_TYPE.md) enumeration that specifies whether the reference type is strong or weak.  
  
 m_pReference  
 An [IDebugReference2](../vs140/IDebugReference2.md) object that specifies the reference information.  
  
## Remarks  
 This structure is passed to a call to the [IDebugReference2::GetReferenceInfo](../vs140/IDebugReference2--GetReferenceInfo.md) method to be filled in. This structure is also returned as part of a list from the [IEnumDebugReferenceInfo2](../vs140/IEnumDebugReferenceInfo2.md) interface which, in turn, is returned from a call to the [IDebugReference2::EnumChildren](../vs140/IDebugReference2--EnumChildren.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [IDebugReference2](../vs140/IDebugReference2.md)   
 [DEBUGREF_INFO_FLAGS](../vs140/DEBUGREF_INFO_FLAGS.md)   
 [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md)   
 [REFERENCE_TYPE](../vs140/REFERENCE_TYPE.md)   
 [IDebugReference2::GetReferenceInfo](../vs140/IDebugReference2--GetReferenceInfo.md)   
 [IDebugReference2::EnumChildren](../vs140/IDebugReference2--EnumChildren.md)   
 [IEnumDebugReferenceInfo2](../vs140/IEnumDebugReferenceInfo2.md)