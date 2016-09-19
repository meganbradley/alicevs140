---
title: "IEnumDebugReferenceInfo2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7ed01441-686f-4032-8268-a4c750f19f85
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugReferenceInfo2
This interface enumerates [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) structures.  
  
## Syntax  
  
```  
IEnumDebugReferenceInfo2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for references to objects in memory. This interface must be implemented only if references are supported.  
  
## Notes for Callers  
 Visual Studio calls [IDebugReference2::EnumChildren](../vs140/IDebugReference2--EnumChildren.md) to obtain this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugReferenceInfo2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugReferenceInfo2--Next.md)|Retrieves a specified number of [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) structures in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugReferenceInfo2--Skip.md)|Skips a specified number of [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) structures in the enumeration sequence.|  
|[Reset](../vs140/IEnumDebugReferenceInfo2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugReferenceInfo2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugReferenceInfo2--GetCount.md)|Gets the number of [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) structures in an enumerator.|  
  
## Remarks  
 A reference is essentially a type and an address, whereas a property is a name, type, and address. A reference persists as long as the object referred to exists in memory. See [IDebugReference2](../vs140/IDebugReference2.md) for more details.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md)   
 [IDebugReference2](../vs140/IDebugReference2.md)   
 [IDebugReference2::EnumChildren](../vs140/IDebugReference2--EnumChildren.md)