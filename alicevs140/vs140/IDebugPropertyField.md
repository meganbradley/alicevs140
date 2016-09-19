---
title: "IDebugPropertyField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b50edb2c-fb8d-4def-993d-17d23d2027c1
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPropertyField
This interface provides the functions that allow getting and setting a property.  
  
## Syntax  
  
```  
IDebugPropertyField : IDebugContainerField  
```  
  
## Notes for Implementers  
 A symbol provider implements this interface on the same object that implements the [IDebugContainerField](../vs140/IDebugContainerField.md). This interface is a specialization that supports the concept of properties on a class.  
  
## Notes for Callers  
 Use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from the [IDebugContainerField](../vs140/IDebugContainerField.md) interface if the [IDebugField::GetKind](../vs140/IDebugField--GetKind.md) method returns `FIELD_KIND_PROP`.  
  
## Methods in Vtable Order  
 In addition to the methods on the [IDebugField](../vs140/IDebugField.md) and [IDebugContainerField](../vs140/IDebugContainerField.md) interfaces, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[GetPropertyGetter](../vs140/IDebugPropertyField--GetPropertyGetter.md)|Gets the method that gets the property.|  
|[GetPropertySetter](../vs140/IDebugPropertyField--GetPropertySetter.md)|Gets the method that sets the property.|  
  
## Remarks  
 A property is a managed code concept and represents a method that is treated as a variable. Properties do not exist in unmanaged C++.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugContainerField](../vs140/IDebugContainerField.md)