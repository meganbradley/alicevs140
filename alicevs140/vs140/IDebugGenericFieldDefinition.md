---
title: "IDebugGenericFieldDefinition"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b5a853b7-221e-4d62-8948-07423089d75d
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugGenericFieldDefinition
Represents the definition of a field for a managed code generic type.  
  
## Syntax  
  
```  
IDebugGenericFieldDefinition : IUnknown  
```  
  
## Methods  
 This interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugGenericFieldDefinition::ConstructInstantiation](../vs140/IDebugGenericFieldDefinition--ConstructInstantiation.md)|Constructs a field instance given an array of type arguments.|  
|[IDebugGenericFieldDefinition::GetFormalTypeParams](../vs140/IDebugGenericFieldDefinition--GetFormalTypeParams.md)|Retrieves the type parameters given the number of parameters.|  
|[IDebugGenericFieldDefinition::TypeParamCount](../vs140/IDebugGenericFieldDefinition--TypeParamCount.md)|Retrieves the number of type parameters associated with the generic field.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll