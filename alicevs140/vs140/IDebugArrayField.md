---
title: "IDebugArrayField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9667b0a5-4295-46cc-9388-b75c1350be15
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugArrayField
This interface describes an array symbol or type.  
  
## Syntax  
  
```  
IDebugArrayField : IDebugContainerField  
```  
  
## Notes for Implementers  
 The symbol provider implements this interface on the same object that implements the [IDebugContainerField](../vs140/IDebugContainerField.md) interface. This interface is a specialization that represents array objects.  
  
## Notes for Callers  
 Use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from the [IDebugContainerField](../vs140/IDebugContainerField.md) interface if [IDebugField::GetKind](../vs140/IDebugField--GetKind.md) returns the flag `FIELD_TYPE_ARRAY`.  
  
## Methods in Vtable Order  
 In addition to the methods on the [IDebugField](../vs140/IDebugField.md) and [IDebugContainerField](../vs140/IDebugContainerField.md) interfaces, this interface implements the following:  
  
|Method|Description|  
|------------|-----------------|  
|[GetNumberOfElements](../vs140/IDebugArrayField--GetNumberOfElements.md)|Gets the number of elements in the array.|  
|[GetElementType](../vs140/IDebugArrayField--GetElementType.md)|Gets the type of element in the array.|  
|[GetRank](../vs140/IDebugArrayField--GetRank.md)|Gets the rank of the array.|  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugContainerField](../vs140/IDebugContainerField.md)   
 [IDebugField](../vs140/IDebugField.md)