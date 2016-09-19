---
title: "IDebugEnumField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 42f685bf-0f39-47f4-98b0-6022efe2bf97
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEnumField
This interface represents an enumeration type.  
  
## Syntax  
  
```  
IDebugEnumField : IDebugContainerField  
```  
  
## Notes for Implementers  
 A symbol provider implements this interface to represent an enumeration.  
  
## Notes for Callers  
 Use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from the [IDebugField](../vs140/IDebugField.md) interface if [IDebugField::GetKind](../vs140/IDebugField--GetKind.md) returns `FIELD_TYPE_ENUM`.  
  
## Methods in VTable order  
 In addition to the methods on the `IDebugField` and `IDebugContainerField` interfaces, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugEnumField::GetUnderlyingSymbol](../vs140/IDebugEnumField--GetUnderlyingSymbol.md)|Returns an [IDebugField](../vs140/IDebugField.md) describing the name for this enumeration type.|  
|[IDebugEnumField::GetStringFromValue](../vs140/IDebugEnumField--GetStringFromValue.md)|Returns the name of the enumeration constant associated with the given value.|  
|[IDebugEnumField::GetValueFromString](../vs140/IDebugEnumField--GetValueFromString.md)|Returns the value associated with the given enumeration constant name|  
|[IDebugEnumField::GetValueFromStringCaseInsensitive](../vs140/IDebugEnumField--GetValueFromStringCaseInsensitive.md)|Returns the value associated with the given enumeration constant name but ignoring case.|  
  
## Remarks  
 It is the underlying symbol that is actually bound to a location with [IDebugBinder::Bind](../vs140/IDebugBinder--Bind.md).  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugContainerField](../vs140/IDebugContainerField.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [IDebugBinder::Bind](../vs140/IDebugBinder--Bind.md)