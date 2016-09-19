---
title: "IDebugAlias2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5252dcbb-8bfe-4d8a-a8e5-b022b194df19
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugAlias2
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Represents a numeric alias for a variable, and enables an expression evaluator (EE) to obtain the application domain for the alias.  
  
## Syntax  
  
```  
IDebugAlias2 : IDebugAlias  
```  
  
## Notes for Implementers  
 This interface is implemented by the managed debug engine (DE).  
  
## Methods  
 In addition to the methods on the [IDebugAlias](../vs140/IDebugAlias.md) interface, this interface implements the following method:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugAlias2::GetAppDomainId](../vs140/IDebugAlias2--GetAppDomainId.md)|Retrieves the identifier for the application domain.|  
  
## Remarks  
 An alias is a decimal number in string form followed by the # character, for example, 1001#.  
  
## Requirements  
 Header: Ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll