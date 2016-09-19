---
title: "IDebugGenericParamField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba24f499-5ba7-4c67-83e6-923229b52327
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugGenericParamField
Represents a parameter for a managed code generic type.  
  
## Syntax  
  
```  
IDebugGenericParamField : IDebugField  
```  
  
## Notes for Implementers  
 Used for support of generics.  
  
## Methods  
 In addition to the methods on the [IDebugField](../vs140/IDebugField.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugGenericParamField::ConstraintCount](../vs140/IDebugGenericParamField--ConstraintCount.md)|Returns the number of constraints that are associated with this generic parameter.|  
|[IDebugGenericParamField::GetConstraints](../vs140/IDebugGenericParamField--GetConstraints.md)|Retrieves the constraints that are associated with this generic parameter.|  
|[IDebugGenericParamField::GetFlags](../vs140/IDebugGenericParamField--GetFlags.md)|Retrieves the flags for this generic parameter.|  
|[IDebugGenericParamField::GetIndex](../vs140/IDebugGenericParamField--GetIndex.md)|Retrieves the index of this generic parameter.|  
|[IDebugGenericParamField::GetNameOfFormalParam](../vs140/IDebugGenericParamField--GetNameOfFormalParam.md)|Retrieves the name of this generic parameter.|  
|[IDebugGenericParamField::GetOwner](../vs140/IDebugGenericParamField--GetOwner.md)|Retrieves the type or method owner of this generic parameter.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll