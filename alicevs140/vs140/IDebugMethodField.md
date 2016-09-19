---
title: "IDebugMethodField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a7dc9030-fc98-4cf1-b943-37a4003300b6
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugMethodField
This interface describes a method.  
  
## Syntax  
  
```  
IDebugMethodField : IDebugContainerField  
```  
  
## Notes for Implementers  
 A symbol provider implements this interface on the same object that implements the [IDebugContainerField](../vs140/IDebugContainerField.md) interface. This interface is a specialization that presents a method.  
  
## Notes for Callers  
 Use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from the [IDebugContainerField](../vs140/IDebugContainerField.md) interface if [IDebugField::GetKind](../vs140/IDebugField--GetKind.md) returns `FIELD_TYPE_METHOD`. In addition, the methods, [IDebugPropertyField::GetPropertyGetter](../vs140/IDebugPropertyField--GetPropertyGetter.md), [IDebugPropertyField::GetPropertySetter](../vs140/IDebugPropertyField--GetPropertySetter.md), and [IDebugClassField::EnumConstructors](../vs140/IDebugClassField--EnumConstructors.md), all return the `IDebugMethodField` interface.  
  
## Methods in Vtable Order  
 In addition to the methods on the [IDebugField](../vs140/IDebugField.md) and [IDebugContainerField](../vs140/IDebugContainerField.md) interfaces, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[EnumParameters](../vs140/IDebugMethodField--EnumParameters.md)|Creates an enumerator for the parameters of the method.|  
|[GetThis](../vs140/IDebugMethodField--GetThis.md)|Gets the "this" pointer of the object containing the method.|  
|[EnumAllLocals](../vs140/IDebugMethodField--EnumAllLocals.md)|Creates an enumerator for all local variables of the method.|  
|[EnumLocals](../vs140/IDebugMethodField--EnumLocals.md)|Creates an enumerator for selected local variables of the method.|  
|[IsCustomAttributeDefined](../vs140/IDebugMethodField--IsCustomAttributeDefined.md)|Determines whether a specific custom attribute has been defined.|  
|[EnumStaticLocals](../vs140/IDebugMethodField--EnumStaticLocals.md)|Creates an enumerator for static local variables of the method.|  
|[GetGlobalContainer](../vs140/IDebugMethodField--GetGlobalContainer.md)|Gets the global container of the method.|  
|[EnumArguments](../vs140/IDebugMethodField--EnumArguments.md)|Creates an enumerator for the type of each argument required to call the method.|  
  
## Remarks  
 A method can contain parameters as well as local variables.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugContainerField](../vs140/IDebugContainerField.md)   
 [IDebugField](../vs140/IDebugField.md)