---
title: "Symbol Provider Interfaces"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4201f10e-c9f7-4b38-bb45-40fe0082d5bf
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Symbol Provider Interfaces
The following are the Symbol Handling Interfaces for the [!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)].  
  
## Discussion  
 These interfaces are used to evaluate variables in a call stack during break mode. They are implemented only for common language runtime symbol providers (SP).  
  
|Interface|Implemented by|Description|  
|---------------|--------------------|-----------------|  
|[IDebugAddress](../vs140/IDebugAddress.md)|SP|Represents the address of an item.|  
|[IDebugAddress2](../vs140/IDebugAddress2.md)|SP|Represents the address of an item, providing access to the process ID.|  
|[IDebugArrayField](../vs140/IDebugArrayField.md)|SP|Represents an array symbol or array type.|  
|[IDebugClassField](../vs140/IDebugClassField.md)|SP|Represents a class symbol or class type.|  
|[IDebugComPlusSymbolProvider](../vs140/IDebugComPlusSymbolProvider.md)|SP|Represents a COM+ symbol provider with methods that are specific to managed code.|  
|[IDebugComPlusSymbolProvider2](../vs140/IDebugComPlusSymbolProvider2.md)|SP|Represents a COM+ symbol provider with methods that are specific to managed code and extends the **IDebugComPlusSymbolProvider**.|  
|[IDebugContainerField](../vs140/IDebugContainerField.md)|SP|Represents a symbol or type that is a container for other symbols or types.|  
|[IDebugCustomAttribute](../vs140/IDebugCustomAttribute.md)|SP|Represents a custom attribute that can be attached to a symbol.|  
|[IDebugCustomAttributeQuery](../vs140/IDebugCustomAttributeQuery.md)|SP|Represents a query for custom attributes on a method or type.|  
|[IDebugCustomAttributeQuery2](../vs140/IDebugCustomAttributeQuery2.md)|SP|Provides access to custom attributes on a symbol.|  
|[IDebugDynamicField](../vs140/IDebugDynamicField.md)|SP|The base interface for any type that can be determined at runtime.|  
|[IDebugDynamicFieldCOMPlus](../vs140/IDebugDynamicFieldCOMPlus.md)|SP|Represents a dynamic field for an [IDebugBinder](../vs140/IDebugBinder.md) object.|  
|[IDebugEnumField](../vs140/IDebugEnumField.md)|SP|Represents an enumeration type.|  
|[IDebugExtendedField](../vs140/IDebugExtendedField.md)|Sp|Extends the types of available fields to support managed code generics.|  
|[IDebugField](../vs140/IDebugField.md)|SP|The base class for all fields; represents a description of a symbol or type.|  
|[IDebugGenericFieldDefinition](../vs140/IDebugGenericFieldDefinition.md)|SP|Represents the definition of a field for a managed code generic type.|  
|[IDebugGenericFieldInstance](../vs140/IDebugGenericFieldInstance.md)|SP|Represents an instance of a field for a managed code generic type.|  
|[IDebugGenericParamField](../vs140/IDebugGenericParamField.md)|SP|Represents a parameter for a managed code generic type.|  
|[IDebugMethodField](../vs140/IDebugMethodField.md)|SP|Represents a method.|  
|[IDebugModOpt](../vs140/IDebugModOpt.md)|SP|Represents a debug optional modifier.|  
|[IDebugPointerField](../vs140/IDebugPointerField.md)|SP|Represents a pointer.|  
|[IDebugPrimitiveTypeField](../vs140/IDebugPrimitiveTypeField.md)|SP|Represents a primitive type enumeration value from an [IDebugField](../vs140/IDebugField.md) interface.|  
|[IDebugPropertyField](../vs140/IDebugPropertyField.md)|SP|Represents a property of a managed code class that can be get or set.|  
|[IDebugSymbolProvider](../vs140/IDebugSymbolProvider.md)|SP|Represents a symbol provider that provides symbols and types.|  
|[IDebugSymbolProviderDirect](../vs140/IDebugSymbolProviderDirect.md)|SP|Represents a symbol provider with direct access to metadata and core symbol interfaces.|  
|[IDebugTypeFieldBuilder](../vs140/IDebugTypeFieldBuilder.md)|SP|Represents the ability to create a field that represents a type.|  
|[IDebugTypeFieldBuilder2](../vs140/IDebugTypeFieldBuilder2.md)|SP|Extends the **IDebugTypeFieldBuilder** to be able to create array types.|  
|[IEnumDebugAddresses](../vs140/IEnumDebugAddresses.md)|SP|Represents a collection of [IDebugAddress](../vs140/IDebugAddress.md) objects.|  
|[IEnumDebugCustomAttributes](../vs140/IEnumDebugCustomAttributes.md)|SP|Represents a collection of [IDebugCustomAttribute](../vs140/IDebugCustomAttribute.md) objects.|  
|[IEnumDebugFields](../vs140/IEnumDebugFields.md)|SP|Represents a collection of [IDebugField](../vs140/IDebugField.md) objects.|  
  
## See Also  
 [API Reference](../vs140/API-Reference--Visual-Studio-Debugging-.md)