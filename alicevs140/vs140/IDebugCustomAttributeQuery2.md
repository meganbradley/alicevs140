---
title: "IDebugCustomAttributeQuery2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7cfa23e4-a05a-47a3-af6c-bd40c655014b
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCustomAttributeQuery2
Determines the existence of a custom attribute for this field and, if it exists, returns the attribute information.  
  
## Syntax  
  
```  
IDebugCustomAttributeQuery2 : IDebugCustomAttributeQuery  
```  
  
## Notes for Implementers  
 A symbol provider implements this interface on the same object that implements [IDebugField](../vs140/IDebugField.md) in order to support custom attributes.  
  
## Notes for Callers  
 Use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from the [IDebugField](../vs140/IDebugField.md) interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of the **IDebugCustomAttributeQuery** interface.  
  
|Method|Description|  
|------------|-----------------|  
|[IsCustomAttributeDefined](../vs140/IDebugCustomAttributeQuery2--IsCustomAttributeDefined.md)|Determines whether a custom attribute exists by name.|  
|[GetCustomAttributeByName](../vs140/IDebugCustomAttributeQuery2--GetCustomAttributeByName.md)|Gets the attribute information for the given custom attribute.|  
  
 In addition to the **IDebugCustomAttributeQuery** methods, `IDebugCustomAttributeQuery2` implements the following method:  
  
|Method|Description|  
|------------|-----------------|  
|[EnumCustomAttributes](../vs140/IDebugCustomAttributeQuery2--EnumCustomAttributes.md)|Gets an enumerator for all custom attributes attached to this field.|  
  
## Remarks  
 The [IEnumDebugCustomAttributes](../vs140/IEnumDebugCustomAttributes.md) method can return an enumerator for all custom attributes defined for this field.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [IEnumDebugCustomAttributes](../vs140/IEnumDebugCustomAttributes.md)