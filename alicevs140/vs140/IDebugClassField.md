---
title: "IDebugClassField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 49358cbc-8973-4862-9dcc-79b1248e6712
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugClassField
This interface represents a class as a type.  
  
## Syntax  
  
```  
IDebugClassField : IDebugContainerField  
```  
  
## Notes for Implementers  
 A symbol provider implements this interface on the same object that implements the [IDebugContainerField](../vs140/IDebugContainerField.md) interface. This interface is a specialization that represents a class type.  
  
## Notes for Callers  
 A number of interfaces have methods that can return this interface including [IDebugSymbolProvider](../vs140/IDebugSymbolProvider.md), [IDebugMethodField](../vs140/IDebugMethodField.md), and [IDebugCustomAttribute](../vs140/IDebugCustomAttribute.md). Also, you can use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from the [IDebugContainerField](../vs140/IDebugContainerField.md) interface if the [IDebugField::GetKind](../vs140/IDebugField--GetKind.md) method returns the flag `FIELD_TYPE_CLASS`.  
  
## Methods in Vtable Order  
 In addition to the methods on the [IDebugField](../vs140/IDebugField.md) and [IDebugContainerField](../vs140/IDebugContainerField.md) interfaces, this interface implements the following:  
  
|Method|Description|  
|------------|-----------------|  
|[EnumBaseClasses](../vs140/IDebugClassField--EnumBaseClasses.md)|Creates an enumerator for the base classes of this class.|  
|[DoesInterfaceExist](../vs140/IDebugClassField--DoesInterfaceExist.md)|Determines if a specific interface is defined in the class.|  
|[EnumNestedClasses](../vs140/IDebugClassField--EnumNestedClasses.md)|Creates an enumerator for the nested classes of this class.|  
|[GetEnclosingClass](../vs140/IDebugClassField--GetEnclosingClass.md)|Gets the class that encloses this class.|  
|[EnumInterfacesImplemented](../vs140/IDebugClassField--EnumInterfacesImplemented.md)|Creates an enumerator for the interfaces implemented by this class.|  
|[EnumConstructors](../vs140/IDebugClassField--EnumConstructors.md)|Creates an enumerator for the constructors of this class.|  
|[GetDefaultIndexer](../vs140/IDebugClassField--GetDefaultIndexer.md)|Gets the name of the default indexer.|  
|[EnumNestedEnums](../vs140/IDebugClassField--EnumNestedEnums.md)|Creates an enumerator for the nested enumerators of this class.|  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugContainerField](../vs140/IDebugContainerField.md)