---
title: "IDebugPointerField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d51bd5b2-f18e-4e27-b4fb-e6f652fbf635
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPointerField
This interface represents a pointer type.  
  
## Syntax  
  
```  
IDebugPointerField : IDebugContainerField  
```  
  
## Notes for Implementers  
 The symbol provider implements this interface to represent a pointer.  
  
## Notes for Callers  
 Use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from the [IDebugField](../vs140/IDebugField.md) interface if [IDebugField::GetKind](../vs140/IDebugField--GetKind.md) returns `FIELD_TYPE_POINTER`.  
  
## Methods in Vtable order  
 In addition to the methods on the `IDebugField` and `IDebugContainerField` interfaces, this interface implements the following method:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugPointerField::GetDereferencedField](../vs140/IDebugPointerField--GetDereferencedField.md)|Returns an [IDebugField](../vs140/IDebugField.md) describing the target of the pointer.|  
  
## Remarks  
 In C/C++, a pointer can be a container if it is used with array notation. For example, given `char *pString`, `pString` has a type of pointer to `char`. `pString[3]` has the type of a container that is a pointer to `char` that references the fourth element of that container.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [IDebugContainerField](../vs140/IDebugContainerField.md)